## All the Layers Working in Unison

Now that you know the basics of how every layer of out network model works, let's go through an exercise to look at how everything works at every step of the way. Spoiler alert, things are about to get a little geeky, in a good way. Imagine three networks, network A will contain address space 10.1.1.0/24. Network B Will contain address space 192.168.1.0/24, and network C will be 172.16.1.0/24. Router A sits between network A and network B. With an interface configured with an IP of 10.1.1.1 on network A, and an interface at 192.168.1.254 on network B. There's a second router, router B, which connects networks B and C. It has an interface on network B with an IP address of 192.168.1.1, and an interface on network C with an IP address of 172.16.1.1. Now let's put a computer on one of the networks. Imagine it's a desktop, sitting on someone's desk at the workplace. It'll be our client in this scenario, and we'll refer to it as computer 1. It's part of Network A and has been assigned an IP address of 10.1.1.100. Now, let's put another computer on one of our other networks. This one is a server in a data center, it'll act as our server in this scenario, and we'll refer to it as computer 2. It's part of network C, and has been assigned an IP address of 172.16.1.100, and has a web server listening on port 80. An end user sitting at computer 1 opens up a web browser and enters 172.16.1.100 into the address bar, let's see what happens. The web browser running on computer 1 knows it's been ordered to retrieve a web page from 172.16.1.100. The web browser communicates with the local networking stack, which is the part of the operating system responsible for handling networking functions. The web browser explains that it's going to want to establish a TCP connection to 172.16.1.100, port 80. The networking stack will now examine its own subnet. It sees that it lives on the network 10.1.1.0/24, which means that the destination 172.16.1.100 is on another network. At this point, computer 1 knows that it'll have to send any data to its gateway for routing to a remote network. And it's been configured with a gateway of 10.1.1.1. Next, computer 1 looks at its ARP table to determine what MAC address of 10.1.1.1 is, but it doesn't find any corresponding entry. Uh-oh, it's okay, computer A crafts an ARP request for an IP address of 10.1.1.1, which it sends to the hardware broadcast address of all Fs. This ARP discovery request is sent to every node on the local network. When router A receives this ARP message, it sees that it's the computer currently assigned the IP address of 10.1.1.1. So it responds to computer 1 to let it know about its own MAC address of 00:11:22:33:44:55. Computer 1 receives this response and now knows the hardware address of its gateway. This means that it's ready to start constructing the outbound packet. Computer 1 knows that it's being asked by the web browser to form an outbound TCP connection, which means it'll need an outbound TCP port. The operating system identifies the ephemeral port of 50000 as being available, and opens a socket connecting the web browser to this port. Since this is a TCP connection, the networking stack knows that before it can actually transmit any of the data the web browser wants it to, it'll need to establish a connection. The networking stack starts to build a TCP segment. It fills in all the appropriate fields in the header, including a source port of 50000 and a destination port of 80. A sequence number is chosen and is used to fill in the sequence number field. Finally, the SYN flag is set, and a checksum for the segment is calculated and written to the checksum field. Our newly constructed TCP segment is now passed along to the IP layer of the networking stack. This layer constructs an IP header. This header is filled in with the source IP, the destination IP, and a TTL of 64, which is a pretty standard value for this field. Next, the TCP segment is inserted as the data payload for the IP datagram. And a checksum is calculated for the whole thing. Now that the IP datagram has been constructed, computer 1 needs to get this to its gateway, which it now knows has a MAC address of 00:11:22:33:44:55, so an Ethernet Datagram is constructed. All the relevant fields are filled in with the appropriate data, most notably, the source and destination MAC addresses. Finally, the IP datagram is inserted as the data payload of the Ethernet frame, and another checksum is calculated. Now we have an entire Ethernet frame ready to be sent across the physical layer. The network interface connected to computer 1 sends this binary data as modulations of the voltage of an electrical current running across a CAT6 cable that's connected between it and a network switch. This switch receives the frame and inspects the destination MAC address. The switch knows which of its interfaces this MAC address is attached to, and forwards the frame across only the cable connected to this interface. At the other end of this link is router A, which receives the frame and recognizes its own hardware address as the destination. Router A knows that this frame is intended for itself. So it now takes the entirety of the frame and calculates a checksum against it. Router A compares this checksum with the one in the Ethernet frame header and sees that they match. Meaning that all of the data has made it in one piece. Next, Router A strips away the Ethernet frame, leaving it with just the IP datagram. Again, it performs a checksum calculation against the entire datagram. And again, it finds that it matches, meaning all the data is correct. It inspects the destination IP address and performs a lookup of this destination in its routing table. Router A sees that in order to get data to the 172.16.1.0/24 network, the quickest path is one hop away via Router B, which has an IP of 192.168.1.1. Router A looks at all the data in the IP datagram, decrements the TTL by 1, calculates a new checksum reflecting that new TTL value, and makes a new IP datagram with this data. Router B knows that it needs to get this datagram to router B, which has an IP address of 192.168.1.1. It looks at its ARP table, and sees that it has an entry for 192.168.1.1. Now router A can begin to construct an Ethernet frame with the MAC address of its interface on network B as the source. And the MAC address on router B's interface on network B as the destination. Once the values for all fields in this frame have been filled out, router A places the newly constructed IP datagram into the data payload field. Calculates a checksum, and places this checksum into place, and sends the frame out to network B. Just like before, this frame makes it across network B, and is received by router B. Router B performs all the same checks, removes the the Ethernet frame encapsulation, and performs a checksum against the IP datagram. It then examines the destination IP address. Looking at its routing table, router B sees that the destination address of computer 2, or 172.16.1.100, is on a locally connected network. So it decrements the TTL by 1 again, calculates a new checksum, and creates a new IP datagram. This new IP datagram is again encapsulated by a new Ethernet frame. This one with the source and destination MAC address of router B and computer 2. And the whole process is repeated one last time. The frame is sent out onto network C, a switch ensures it gets sent out of the interface that computer 2 is connected to. Computer 2 receives the frame, identifies its own MAC address as the destination, and knows that it's intended for itself. Computer 2 then strips away the Ethernet frame, leaving it with the IP datagram. It performs a CRC and recognizes that the data has been delivered intact. It then examines the destination IP address and recognizes that as its own. Next, computer 2 strips away the IP datagram, leaving it with just the TCP segment. Again, the checksum for this layer is examined, and everything checks out. Next, computer 2 examines the destination port, which is 80. The networking stack on computer 2 checks to ensure that there's an open socket on port 80, which there is. It's in the listen state, and held open by a running Apache web server. Computer 2 then sees that this packet has the SYN flag set. So it examines the sequence number and stores that, since it'll need to put that sequence number in the acknowledgement field once it crafts the response. After all of that, all we've done is get a single TCP segment containing a SYN flag from one computer to a second one. Everything would have to happen all over again for computer 2 to send a SYN-ACK response to computer 1. Then everything would have to happen all over again for computer 1 to send an ACK back to computer 2, and so on and so on. Looking at all of this end to end hopefully helps show how all the different layers of our networking model have to work together to get the job done. I hope it also gives you some perspective in understanding how remarkable computer networking truly is. Even more remarkable than that, you [LAUGH] for making it through this module. Now it's time to apply your new knowledge to the next assessment. When you're done, I'll see in the next video, but first, another quiz, you got this. But even if you don't, just review the material until you get more comfortable with this stuff.



现在，您已经了解了网络模型中每个层的工作原理的基础知识，让我们 通过一个练习来了解一切工作在过程中的每一步都是如何工作的。 扰流板警报，事情即将变得有点怪异，在一个很好的方式。 想象一下三个网络，网络 A 将包含地址空间 10.1.1.0/24。 网络 B 将包含地址空间 192.168.1.0/24 ，网络 C 将为 172.16.1.0/24。 路由器 A 位于网络 A 和网络 B 之间，网络A 上的 IP 配置为 10.1.1.1，网络 B 上的接口为 192.168.1.254。第二台路由器路由器 B，用于连接网络 B 和网络 C。 它在网络 B 上有一个 IP 地址为 192 的接口。以 及网络 C 上的一个接口，IP 地址为 172.16.1.1 的接口。 现在让我们把一台计算机放在其中一个网络上。 想象一下，它是一个桌面，坐在工作场所某人的办公桌上。 这 将是我们的客户在这种情况下，我们将它称为计算机 1。 它是网络 A 的一部分，已分配 IP 地址 10.1.1.100。 现在，让我们把另一台计算机放在我们的其他网络上。这是一个数据中心的服务器，在这种情况下它将充当我们的服务器， 我们将它称为计算机 2。 它是网络 C 的一部分，已被分配了一个 172.16.1.100 的 IP 地址，并且有一个 Web 服务器侦听端口 80。 坐在计算机 1 的最终用户打开一个 Web 浏览器，并在 地址栏中输入 172.16.1.100，让我们来看看会发生什么。 计算机 1 上运行的 Web 浏览器知道它已被命令 从 172.16.1.100 检索网页。 Web 浏览器与本地网络堆栈进行通信，该堆栈是 操作系统中负责处理网络功能的一部分。 Web 浏览器解释说 ，它希望建立到 172.16.1.100 端口 80 的 TCP 连接。 网 络堆栈现在将检查自己的子网。 它发现它位于网络 10.1.1.0/24， 这意味着目标 172.16.1.100 位于另一个网络上。 此时，计算机 1 知道它必须将任何数据发送到其网关，以便 路由到远程网络。 它已配置为 10.1.1.1 的网关。 接下来，计算机 1 查看其 ARP 表以确定 10.1.1.1 的 MAC 地址，但找不到任何相应的条目。 嗯，没关系，计算机 A 为 10.1.1.1 的 IP 地址制作了 ARP 请求， 它发送到所有 Fs 的硬件广播地址。 此 ARP 发现请求将发送到本地网络上的每个节点。当路由器 A 收到此 ARP 消息时，它会看到它是当 前分配的 IP 地址 10.1.1.1 的计算机。 所以它响应计算机 1，让它知道它 自己的 MAC 地址 00:11:22:33:44:55。 计算机 1 收到此响应，现在知道其网关的硬件地址。 这意味着它已准备好开始构建出站数据包。计算机 1 知道 Web 浏览器要求它构建 出站 TCP 连接，这意味着它需要一个出站 TCP 端口。 操作系统将 50000 的临时端口标识为 可用，并打开将 Web 浏览器连接到此端口的套接字。由于这是一个 TCP 连接，因此网络堆栈知道 ，在实际传输 Web 浏览器想要的任何数据之前， 它需要建立连接。 网络堆栈开始构建 TCP 段。 它填充标头中的所有相应字段， 包括源端口 50000 和目标端口 80。 选择序列号并用于填写序列号字段。 最后，设置 SYN 标志，并计算段的校验和并 写入校验和字段。我们新构建的 TCP 段现在传递到 网络堆栈的 IP 层。 此层构建一个 IP 标头。 此标头填充了源 IP、目标 IP 和 TTL 64，这对于此字段来说是一个非常标准的值。接下来，将 TCP 段插入为 IP 数据报的数据负载。 并为整个事情计算校验和。 现在已经构建了 IP 数据报， 计算机 1 需要将其传送到其网关，它现在知道 该网关的 MAC 地址为 00:11:22:33:44:55， 因此构建了一个以太网数据报。 所有相关字段都填写了相应的数据，最明显的是 源 MAC 地址和目的 MAC 地址。最后，将 IP 数据报插入作为以太网帧的数据有效负载， 并计算另一个校验和。现在，我们有一个整个以太网帧可以通过物理层发送。连接到计算机 1 的网络接口将此二进制数据 作为电流电压的调制发送，该电 缆通过连接在计算机和网络交换机之间的 CAT6 电缆运行。此交换机接收帧并检查目的 MAC 地址。 交换机知道此 MAC 地址连接到哪个接口， 并仅通过连接到此接口的电缆转发帧。此链路的另一端是路由器 A，它接收帧并将 其自己的硬件地址识别为目的地。路由器 A 知道此帧是专为自身设计的。 所以它现在需要整个帧并计算对其进行校验和。 路由器 A 将此校验和与以太网帧标头中的校验和进行比较，并发 现它们是否匹配。 这 意味着所有的数据已经成为一块。 接下来，路由器 A 会剥离以太网帧 ，只留下 IP 数据报。 同 样，它对整个数据报执行校验和计算。 再次，它发现它匹配，意味着所有的数据都是正确的。 它会检查目的 IP 地址 ，并在其路由表中执行此目的地的查找。 路 由器 A 发现，为了将数据传输到 172.16.1.0/24 网络，最快的路径是通过路由器 B 一跳，路由器 B 的 IP 为 192.168.1.1。 路由器 A 查看 IP 数据报中的所有数据，将 TTL 递减 1，计算反映新 TTL 值的新校验和，并使用此数据创建新的 IP 数据报。路由器 B 知道它需要将此数据报传送到路由器 B， 该路由器的 IP 地址为 192.168.1.1。 它查看其 ARP 表，并发现它有 192.168.1.1 的条目。 现在，路由器 A 可以开始构建以太网帧， 其接口在网络 B 上的 MAC 地址作为源。 网络 B 上路由器 B 接口上的 MAC 地址作为目的地。 填写此帧中所有字段的值后， 路由器 A 会将新构建的 IP 数据报放入数据负载字段中。 计算校验和，并将此校验和放置到位，然后将 帧发送到网络 B。就像以前一样，此帧通过网络 B 进行，并 由路由器 B 接收。 路由器 B 执行所有相同的检查，删除以太网 帧封装，并执行对 IP 数据报的校验和。然后检查目标 IP 地址。 查 看其路由表，路由器 B 发现计算机 2（即 172.16.1.100）的目的地址位于本地连接的网络上。 所以它再次减少 TTL 1，计算一个新的校验和，并 创建一个新的 IP 数据报。 这个新的 IP 数据报再次被一个新的以太网帧封装。 这是路由器 B 和计算机 2 的源 MAC 地址和目标 MAC 地址。 和整个过程是重复的最后一次。 帧被发送到网络 C， 交换机确保从计算机 2 连接的接口发送出来。 计算机 2 接收帧，将其自己的 MAC 地址识别为目的地， 并知道它是针对自己的。 然后，计算机 2 剥离以太网帧，将其留在 IP 数据报中。 它执行 CRC 并确认数据已完好无损地交付。 然后，它会检查目标 IP 地址并将其识别为自己的地址。接下来，计算机 2 剥离 IP 数据报 ，只留下 TCP 段。 再次检查此图层的校验和，并检出所有内容。 接下来，计算机 2 检查目标端口，即 80。 计算机 2 上的网络堆栈进行检查 ，以确保端口 80 上有一个打开的套接字。 它处于侦听状态，并由正在运行的 Apache Web 服务器保持打开状态。 然后，计算机 2 看到此数据包具有设置的 SYN 标志。 因 此，它会检查序列号并存储该序列号，因为 一旦它完成响应，它就需要将该序列号放在确认字段中。在所有这些之后，我们所做的就是 从一台计算机获得一个包含 SYN 标志的 TCP 段。计算机 2 向计算机 1 发送 SYN-ACK 响应，一切都必须重新发生。 然后，一切都必须重新发生， 计算机 1 将 ACK 发送回计算机 2，依此类推。看看所有这一切有希望有助于展示 我们网络模型的所有不同层次如何协同工作才能完成工作。 我希望它也能为您提供一些观点，让您了解计算机 网络的真正卓越性。 甚至更显着的是，你 [笑] 为它通过这个模块。 现在是时候将您的新知识应用到下一次评估中了。 当你完成后，我会在下一个视频中看到，但首先，另一个测验， 你得到了这个。 但是，即使你不这样做， 只要检查材料，直到你得到更加舒适的这些东西。