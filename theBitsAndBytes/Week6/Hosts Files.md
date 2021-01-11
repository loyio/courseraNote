## Hosts Files

Long before DNS was an established and globally available technology, it was clear to computer operators that they needed a language based system to refer to network devices. We've talked about how humans are way better at remembering descriptive words than numbers, but numbers represent the natural way that computers think and communicate. The original way that numbered network addresses were correlated with words was through hosts files. A host file is a flat file that contains, on each line, a network address followed by the host name. It can be referred to as. For example, a line in a host file might read 1.2.3.4 webserver. This means that on the computer where this host file resides, a user could just refer to webserver instead of the IP one dot two dot three dot four. Hosts files are evaluated by the networking stack of the operating system itself. That means the presence of an entry there would translate to anywhere you might refer to a networking address. Sticking with our earlier example, a user could type web server into a web browser URL bar, or could issue a Ping web webserver command and it would get translated to one dot two dot three dot four in either case. Hosts files might be ancient technology, but they've stuck around all this time. All modern operating systems, including those that power our phone and tablets, still have hosts files. One reason is because of a special IP address we haven't covered yet. The loopback address. A loopback address always points to itself, so a loopback address is a way of sending network traffic to yourself. Sending traffic to a loop back address bypasses all network infrastructure itself and traffic like that never leaves the node. The loop back IP for IPV 4 is 127.0.0.1 and it's still to this day configured on every modern operating system through an entry in a hosts file. Almost every hosts file in existence will in the very least, contain a line that reads 127.0.0.1 localhost. Most likely followed by ::1 localhost where ::1 is the loop back address for IPv 6. Since DNS is everywhere, hosts files aren't used much anymore, but they still exist and they're still important to know about. Some software even requires specific entries in the hosts file to operate properly as antiquated as this practice may seem. Finally, host files are a popular way for computer viruses to disrupt and redirect users' traffic. It's not a great idea to use host files today, but they do have some useful troubleshooting purposes that can be helpful in IT support. Host files are examined before a DNS resolution attempt occurs on just about every major operating system. This let's you force an individual computer to think a certain domain name always points at a specific IP, got it? We've covered a lot, so take time to go back if you need to. And make sure you understand the concepts we're discussing. Next up a short quiz.



早在 DNS 成为一种全球可用的技术之前， 计算机运营商很清楚他们需要一个基于语言的系统 来引用网络设备。 我们已经讨论过人类在记忆描述性 词汇方面比数字更好，但数 字代表了计算机思考和沟通的自然方式。 编号网络地址与单词关联的原始方式是 通过主机文件。 主机文件是一个平面文件，每行都包含 一个网络地址，后跟主机名。 它可以称为. 例如，主机文件中的一行可能会读取 1.2.3.4 Web 服务器。 这意味着在此主机文件所在的计算机上，用户可以 只引用 Web 服务器而不是 IP 一点二点三点四。 主机文件由操作系统 本身的网络堆栈进行评估。 这意味着该条目的存在将转换为 您可能指向网络地址的任何位置。 坚持我们之前的例子，用户可以在 Web 浏览器 URL 栏中键入 Web 服务器，或者发出 Ping Web Web 服务器命令，并 且在任何情况下都会被翻译为一点二点三点四。主机文件可能是古老的技术，但他们一直坚持不移。 所有现代操作系统，包括那些为我们的手机和 平板电脑供电的操作系统，仍然有主机文件。 其中 一个原因是我们尚未覆盖的特殊 IP 地址。 环回地址。 环回地址始终指向自己，因此 环回地址是向自己发送网络流量的一种方式。 将 流量发送到回路地址会绕过所有网络 基础架构本身，像这样的流量永远不会离开节点。IPV 4 的回路 IP 是 127.0.0.1，到目前为止， 它仍然是 通过主机文件中的条目在每个现代操作系统上配置的。 几乎每个存在的主机文件至少包 含一行读取 127.0.0.1 本地主机。 最有可能接下来是። 1 本地主机，其中 ። 1 是 IPV 6 的环路回地址。由于 DNS 无处不在，因此主机文件已不再使用了，但 它们仍然存在，它们仍然需要了解。 有些软件甚至需要在 hosts 文件中的特定条目才能 正常运行，因为这种做法可能看起来像过时一样。 最后，主机文件是计算机病毒中断和 重定向用户流量的常用方式。 现在使用主机文件并不是一个好主意，但它们确实有一些有用的故障排除目的，可以帮助 IT 支持。 在几乎每个主要操作系统上进行 DNS 解析尝试之前，会检查主机文件。 这让你强制一台计算机认为某个域名 总是指向某个特定的 IP，明白吗？ 我们已经介绍了很多，所以如果需要，请花时间回去。 并确保您了解我们正在讨论的概念。 接下来是一个简短的测验。