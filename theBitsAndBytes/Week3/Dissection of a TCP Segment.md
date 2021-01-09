## Dissection of a TCP Segment

Heads up. In this video, we're going to dissect a TCP segment. In IT support, if network traffic isn't behaving as users expect it to, you might have to analyze it closely to troubleshoot. So, get ready to take a peek at all the inner workings. Just like how an Ethernet frame encapsulates an IP datagram, an IP datagram encapsulates a TCP segment. Remember that an Ethernet frame has a payload section which is really just the entire contents of an IP datagram. Remember also that an IP datagram has a payload section and this is made up of what's known as a TCP segment. A TCP segment is made up of a TCP header and a data section. This data section, as you might guess, is just another payload area for where the application layer places its data. A TCP header itself is split into lots of fields containing lots of information. First, we have the source port and the destination port fields. The destination port is the port of the service the traffic is intended for, which we talked about in the last video. A source port is a high numbered port chosen from a special section of ports known as ephemeral ports. We'll cover ephemeral ports in more detail in a little bit. For now, it's enough to know that a source port is required to keep lots of outgoing connections separate. You know how a destination port, say port 80, is needed to make sure traffic reaches a web server running on a certain IP? Similarly, a source port is needed so that when the web server replies, the computer making the original request can send this data to the program that was actually requesting it. It is in this way that when it web server responds to your requests to view a webpage that this response gets received by your web browser and not your word processor. Next up is a field known as the sequence number. This is a 32-bit number that's used to keep track of where in a sequence of TCP segments this one is expected to be. You might remember that lower on our protocol stack, there are limits to the total size of what we send across the wire. In Ethernet frame, it's usually limited in size to 1,518 bytes, but we usually need to send way more data than that. At the transport layer, TCP splits all of this data up into many segments. The sequence number in a header is used to keep track of which segment out of many this particular segment might be. The next field, the acknowledgment number, is a lot like the sequence number. The acknowledgment number is the number of the next expected segment. In very simple language, a sequence number of one and an acknowledgement number of two could be read as this is segment one, expect segment two next. The data offset field comes next. This field is a four-bit number that communicates how long the TCP header for this segment is. This is so that the receiving network device understands where the actual data payload begins. Then, we have six bits that are reserved for the six TCP control flags. We'll cover the control flags and what they each mean in the next video, so flag this for later. The next field is a 16-bit number known as the TCP window. A TCP window specifies the range of sequence numbers that might be sent before an acknowledgement is required. As we'll cover in more details soon, TCP is a protocol that's super reliant on acknowledgements. This is done in order to make sure that all expected data is actually being received and that the sending device doesn't waste time sending data that isn't being received. The next field is a 16-bit checksum. It operates just like the checksum fields at the IP and Ethernet level. Once all of this segment has been ingested by a recipient, the checksum is calculated across the entire segment and is compared with the checksum in the header to make sure that there was no data lost or corrupted along the way. The Urgent pointer field is used in conjunction with one of the TCP control flags to point out particular segments that might be more important than others. This is a feature of TCP that hasn't really ever seen adoption and you'll probably never find it in modern networking. Even so, it's important to know what all sections of the TCP header are. Next up, we have the options field. Like the urgent pointer field, this is rarely used in the real world, but it's sometimes used for more complicated flow control protocols. Finally, we have some padding which is just a sequence of zeros to ensure that the data payload section begins at the expected location.



抬起头来 在本视频中， 我们将分析一个 TCP 段。 在 IT 支持方面，如果网络流量不像用户预期的那样行为，则 可能需要仔细分析它才能进行故障排除。 所以，准备采取偷看所有的内部运作。 就像以太网帧封装 IP 数据报一样， IP 数据报封装了 TCP 数据段。 请记住，以太网帧有一个有效负载部分， 它实际上只是 IP 数据报的全部内容。 还要记住，IP 数据报有一 个有效负载部分，这是由所谓的 TCP 段组成的。 TCP 段由 TCP 标头和数据部分组成。 您可能会猜到，此数据部分 只是应用程序层放置其数据的另一个有效负载区域。 TCP 标头本身被拆分为包含大量信息的多个字段。 首先，我们有源端口和目的端口字段。 目标端口是流量所针对的服务端口， 我们在上一个视频中谈到了这一点。 源端口是从 称为临时端口的特殊端口部分中选择的编号较高的端口。 我们将更详细地介绍临时端口。 现在，只 需要一个源端口来保持大量传出连接分开就足够了。 您知道如何 需要目标端口（例如端口 80）来确保流量到达某个 IP 上运行的 Web 服务器？ 同样，需要一个源端口，以便当 Web 服务器回复时，发 出原始请求的计算机可以将 此数据发送到实际请求的程序。 正是以这种方式，当 Web 服务器响应您查看网 页的请求时，您的 Web 浏览器而不是您的文字处理器接收此响应。 接下来是一个称为序列号的字段。 这是一 个 32 位数字，用于跟踪 TCP 段序列中预期的位置。 您可能还记得，在我们的协议堆栈中 ，我们通过线路发送的内容的总大小有限制。 在以太网帧中，它的大小通常限制为 1,518 字节， 但我们通常需要发送更多的数据。 在传输层， TCP 将所有这些数据分割为多个段。 标题中的序列号用于跟踪 许多此特定段可能是哪个段。 下一个字段，即确认编号 ，非常类似于序列号。 确认编号是下一个预期段的编号。 在非常简单的语言中 ， 可以读取序列号 1 和确认号为 2，因为这是段 1， 预计段 2 接下来。 接下来是数据偏移字段。 此字段是一个四位数字，用于表达 此段的 TCP 标头的长度。 这样，接收网络设备就可以 了解实际数据负载的开始位置。 然后，我们有六个位保留给六个 TCP 控制标志。 我们将在下一个视频中介绍控制标志以及它们的含义， 所以将其标记为稍后。 下一个字段是称为 TCP 窗口的 16 位数字。 TCP 窗口指定在需 要确认之前可能发送的序列号范围。 正 如我们很快将详细介绍的 那样，TCP 是一个超级依赖于确认的协议。 这样做是为了确保实际上 接收所有预期的数据，并确保发送设备不会 浪费时间发送未接收的数据。 下一个字段是 16 位校验和。 它的工作方式与 IP 和以太网级别的校验和字段一样。 一旦收件人接收了所有这些段，就 会计算整个段的校验和，并与 标头中的校验和进行比较，以确保在此过程中没有数据丢失或损坏。 “ 紧急指针” 字段与其中一个 TCP 控制标志结合使用，以指出 可能比其他更重要的特定段。 这是 TCP 的一项功能，从未真正见 过采用，您可能永远不会在现代网络中找到它。 即便如此，了解 TCP 标头的所有部分都是很重要的。 接下来，我们有选项字段。 与 紧急指针字段一样， 这在现实世界中很少使用， 但它有时用于更复杂的流量控制协议。 最后，我们有一些填充，这只是一个零序列， 以确保数据有效载荷部分从预期位置开始。





![image-20210107182702799](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107pYJ5cd.png)
