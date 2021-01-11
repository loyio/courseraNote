## IPv6 and IPv4 Harmony

It's just not possible for the entire Internet and all connected networks to switch to IPv6 all at once. There would be way too much coordination at play. Too many old devices that might not even know how to speak IPv6 at all, still requiring connections. So the only way IPv6 will ever take hold is to develop a way for IPv6 and IPv4 traffic to coexist at the same time. This would let individual organizations make the transition when they can. One example of how this can work is with what's known as IPv4 mapped address space. The IPv6 specifications have set aside a number of addresses that can be directly correlated to an IPv4 address. Any IPv6 address that begins with 80 zeros, and is then followed by 16 ones is understood to be part of the IPv4 mapped address space. The remaining 32 bits of the IPv6 address is just the same 32 bits of the IPv4 address it's meant to represent. This gives us a way for IPv4 traffic to travel over an IPv6 network. But probably more important is for IPv6 traffic to have a way to travel over IPv4 networks. It's easier for an individual organization to make the move to IPv6 than it is for the networks at the core of the Internet to. So while IPv6 adoption becomes more widespread, it'll need a way to travel over the old IPv4 remnants of the Internet backbone. The primary way this is achieve today is through IPv6 tunnels. IPv6 tunnels are conceptually pretty simple. They consist of IPv6 tunnels servers on either end of a connection. These IPv6 tunnel servers take incoming IPv6 traffic and encapsulate it within traditional IPv4 datagrams. This is then delivered across the IPv4 Internet space where it's received by another IPv6 tunnel server. That server performs the de-encapsulation and passes the IPv6 traffic further along in the network. Along with IPv6 tunnel technologies, the concept of an IPv6 tunnel broker has also emerged. These are companies that provide IPv6 tunneling endpoints for you, so you don't have to introduce additional equipment to your network. There are a lot of competing protocols to be used for these kinds of IPv6 tunnels. Since this is still a new and evolving space, it's not clear who the winner will be. I've left you with some links to read about the main competitors right after this video. It doesn't really matter which tunneling technology ends up becoming the most common solution. It'll probably fade away in time itself. The future of networking is the adoption of IPv6 as the main protocol at the network layer, and one day we won't need any tunnels at all. The future is limitless, and tunnelless, or something like that. You've done an amazing job at getting through all this information. So take some time to pat yourself on the back. You've got one final quiz and a final project to get through. And then you can check this course off your to do list. Are you starting to see the light at the end of the tunnel?



整个互联网和 所有连接的网络都不可能同时切换到 IPv6。 有太多的协调发挥作用。 太多的旧设备甚至根本不知道如何说 IPv6， 仍然需要连接。 因此，IPv6 唯一的方法就是开发一种让 IPv6 和 IPv4 流量同时共存的方法。 这将使个别组织在可能的情况下进行过渡。一个例子是使用所谓的 IPv4 映射地址空间。 IPv6 规范留 出了许多可直接与 IPv4 地址关联的地址。 任何以 80 零开头、后跟 16 个地址的 IPv6 地址都被理解为 IPv4 映射地址空间的一部分。 IPv6 地址的剩余 32 位与所代表的 IPv4 地址的 32 位相同。 这为我们提供了一种 IPv4 流量通过 IPv6 网络传输的方式。 但更重要的是 IPv6 流量能够通过 IPv4 网络传输。 与 互联网核心的网络相比，单个组织更容易迁移到 IPv6。 因此，尽管 IPv6 的采用越来越普遍，但 它需要一种方法来穿越互联网骨干的旧 IPv4 残余物。目前实现这一目标的主要方式是通过 IPv6 隧道。 IPv6 隧道在概念上非常简单。 它们由连接两端的 IPv6 隧道服务器组成。 这些 IPv6 隧道服务器接收传入的 IPv6 流量，并将 其封装在传统的 IPv4 数据报中。 然后通 过 IPv4 互联网空间传送此信息，其中另一个 IPv6 隧道服务器接收该信息。 该服务器执行解封装并 在网络中进一步传递 IPv6 流量。 除了 IPv6 隧道技术 之外，还出现了 IPv6 隧道代理的概念。 这些公司为您提供 IPv6 隧道端点，因此 您无需为您的网络引入额外设备。有许多竞争协议可用于这些类型的 IPv6 隧道。 由于这仍然是一个新的和不断发展 的空间，现在还不清楚谁会是赢家。 我给你留下了一些链接，以阅读关于主要竞争对手的 权利后，这段视频. 哪种隧道技术最 终成为最常见的解决方案并不重要。 它可能会消失的时间本身。 网络的未来是在 网络层采用 IPv6 作为主要协议，有一天我们根本不需要任何隧道。 未来是无限的，没有通道的，或类似的东西。在通过所有这些信息方面，你已经做了一个了不起的工作。 所以需要一些时间拍拍自己的背部。 你有一个最后的测验和一个最后的项目要通过。 然后你可以从你的待办事项列表中查看这门课程。 你开始看到隧道尽头的光了吗？