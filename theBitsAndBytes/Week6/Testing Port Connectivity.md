## Testing Port Connectivity



We've covered a bunch of ways to test connectivity between machines at the network layer. But sometimes, you need to know if things are working at the transport layer. For this, there are two super powerful tools at your disposal. Netcat on Linux and Mac OS and Test-NetConnection on Windows. The Netcat tool can be run through the command nc, and has two mandatory arguments, a host and a port. Running nc google.com 80 would try to establish a connection on port 80 to google.com. If the connection fails, the command will exit. If it succeeds, you'll see a blinking cursor, waiting for more input. This is a way for you to actually send application layered data to the listening service from your own keyboard. If you're really only curious about the status of a report, you can issue the command, with a -Z flag, which stands for Zero Input/Output Mode. A -V flag, which stands for Verbose, is also useful in this scenario. This makes the commands output useful to human eyes as opposed to non-verbose output, which is best for usage in scripts. Side note, verbose basically means talking too much. So, while I bet you want to throw up a flag on me and my jabbering, we still have lots to get through. Okay, so by issuing the Netcat command with the -Z and -V flags, the command's output will simply tell you if a connection to the port in question is possible or not. On Windows, Test-NetConnection is a command with some of the similar functionality. If you run Test-NetConnection with only a host specified, it will default to using an ICMP echo request, much like the program ping. But, it will display way more data, including the data link layer protocol being used. When you issue Test-NetConnection with the -port flag, you can ask it to test connectivity to a specific port. It's important to call out that both Netcat and Test-NetConnection are way more powerful than the brief port connectivity examples we've covered here. In fact, they're such complex tools that covering all of their functionality would be too much for one video. You should read up about all of the other things these super powerful tools can do. We've provided a few in the supplementary readings. And after you've had a chance to read through the material, we'll give you a short quiz.



我们介绍了一系列测试 网络层计算机之间连通性的方法。 但有时候，您需要知道传输层是否有效。 为此，有两个超级强大的工具可供您使用。 在 Linux 和 Mac 操作系统上的网络连接以及在 Windows 上测试网络连接。 Netcat 工具可以通过命令 nc 运行，并具 有两个强制参数：一个主机和一个端口。 运行 NC Google.com 80 会 尝试在端口 80 上建立一个连接到谷歌网站。 如果连接失败，命令将退出。 如果成功，您将看到光标闪烁，等待更多输入。 这是 您从自己的键盘将应用程序分层数据实际发送到侦听服务的一种方法。 如果您真的只 对报告的状态感到好奇，则可以使用-Z 标志发出命令，该标志代表零输入/输出模式。 代表 “详细” 的-V 标志在这种情况下也很有用。 这使得命令输出对人眼有用 ，而不是非详细输出，这最适合在脚本中使用。 侧面说明，冗长基本上意味着说话太多。 所以，虽然我敢打赌，你想在我身上扔一个旗帜，我 们还有很多事情要通过。 好吧，所以通过发出带有-Z 和 -V 标志的 Netcat 命令，命令的输出将简单地告诉您 是否可以连接到有问题的端口。 在 Windows 上， 测试网络连接是一个具有某些类似功能的命令。 如果您只使用指定的主机运行 Test-NetConnection， 则默认使用 ICMP 回应请求，与程序 ping 操作非常相似。 但是，它会显示更多的数据， 包括正在使用的数据链路层协议。 当您发出带有-port 标志的测试网络连接时， 可以要求它测试到特定端口的连接性。 需要指出的 是，Netcat 和测试网络连接都比我们在此介绍的简短端口连接示例更强大。 事实上，它们是如此复杂的工具，覆盖他们的所有 功能对于一个视频来说是太多了。 你应该阅读这些超级强大的工具可以做的所有其他事情。 我们在补充读数中提供了一些。 在你有机会阅读这些材料之后， 我们会给你一个简短的测验。