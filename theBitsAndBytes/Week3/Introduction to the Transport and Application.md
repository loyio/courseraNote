## Introduction to the Transport and Application



The first three layers of our Network Model have helped us describe how individual nodes on a network can communicate with other nodes on either their own network or a remote one. But we haven't discussed how individual computer programs can communicate with each other. It's time to dive into this, because that's really the aim of computer networking. We network computers together, not just so they can send data to each other, but because we want programs running on those computers to be able to send data to each other. This is where the Transport and Application layers of our networking model come into play. In short, the Transport layer allows traffic to be directed to specific network applications. And the Application layer allows these applications to communicate in a way they understand. By the end of this module, you'll be able to describe TCP ports and sockets and identify the different components of a TCP header. You'll also be able to show the difference between connection oriented, and connection lists protocols, and explain how TCP is used to ensure data integrity. Are you ready to be transported to the next lesson? I hope so, because the Transport layer is up next. See you there.





网络模型的前三层帮助我们描述了网络 上的 各个节点如何与其自己的网络或远程网络上的其他节点进行通信。 但我们还没有讨论 单个计算机程序如何相互通信。 现在 是时候深入研究这个问题了， 因为这真的是计算机网络的目的。 我们将计算机联网在一起， 不仅是为了使它们能够相互发送数据， 而是因为我们希望在 这些计算机上运行的程序能够相互发送数据。 这就是 我们网络模型的传输层和应用层发挥作用的地方。 简而言之，传输层允许 将流量定向到特定的网络应用程序。 应 用层允许 这些应用程序以他们理解的方式进行通信。 在 本模块结束时， 您将能够描述 TCP 端口和 套接字，并识别 TCP 标头的不同组件。 您还将能够显示面向连接 和连接列表协议之间的区别， 并解释如何使用 TCP 来确保数据完整性。 你准备好被运送到下一课了吗？ 我希望如此，因为传输层是接下来的。 看到你在那里。