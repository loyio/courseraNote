## NAT, Non-Routable Address Space and the Limits of IPv4

The IANA has been in charge of distributing IP addresses since 1988. Since that time, the internet has expanded at an incredible rate. The 4.2 billion possible IPv4 addresses have been predicted to run out for a long time and they almost have. For some time now, the IANA has primarily been responsible with assigning address blocks to the five regional internet registries or RIRs. The five RIRs are AFRINIC, which serves the continent of Africa, ARIN which serves the United States, Canada and parts of the Caribbean. APNIC, which is responsible for most of Asia, Australia and New Zealand and Pacific Island nations. LACNIC which covers Central and South America and any parts of the Caribbean not covered by ARIN. And finally RIPE, which serves Europe, Russia and the Middle East and portions of Central Asia. These five RIRs have been responsible for assigning IP address blocks to organizations within their geographic areas and most have already run out. The IANA assigned the last unallocated slash eight network blocks to various RIRs on February 3rd, 2011. Then in April 2011, APNIC ran out of addresses. RIPE was next, in September of 2012. LACNIC ran out of addresses to assign in June 2014. And ARIN did the same in September 2015. Only AFNIC has some IPs left, but those are predicted to be depleted by 2018. Wikipedia has a great article all about IPv4 exhaustion and the timelines involved. I've added a link to it in the reading just after this video. This is of course, a major crisis for the internet. IPv6 will eventually resolve these problems and we'll covered in more detail later in this course. But implementing IPv6 worldwide is going to take some time. For now, we wanted to continue to grow and we want more people and devices to connect to it but without IP addresses to assign, a workaround is needed. Spoiler alert, you already know about the major components of this workaround. NAT and non-routable address space. Remember that non-routable address space was defined in RFC1918 and consists of several different IP ranges that anyone can use. And unlimited number of networks can use non-routable address space internally because internet routers won't forward traffic to it. This means there's never any global collision of IP addresses when people use those address spaces. Non-routable address space is largely usable today because of technologies like NAT. With NAT, you can have hundreds even thousands of machines using non-routable address space. Yet, with just a single public IP, all those computers can still send traffic to and receive traffic from the internet. All you need is one single IPv4 address and via NAT, a router with that IP can represent lots and lots of computers behind it. It's not a perfect solution, but until IPv6 becomes more globally available, non-routable address space and NAT will have to do



IANA 自 1988 年以来一直负责分发 IP 地址。 从那时起，互联网已经以令人难以置信的速度扩大。 据预计，42 亿个可能的 IPv4 地址将耗尽 很长一段时间，而且几乎已经用完了。一段时间以来，IANA 主要负责为 五个区域互联网注册机构或 RIR 分配地址块。 这五个 RIR 是非洲信息中心，服务于非洲大陆， ARIN 为美国、加拿大和加勒比部分地区提供服务。 亚太 信息中心, 负责亚洲, 澳大利亚, 新西兰和太平洋岛屿国家的大多数国家. 该网络涵盖中美洲和南美洲以及 加勒比区域信息网不涵盖的任何地区。 最后，RIPE，它服务于欧洲，俄罗斯和 中东和中亚的部分地区。 这五个 RIR 负责为其地理区域 内的组织分配 IP 地址块，大多数已经用完。2011 年 2 月 3 日，IANA 将最后一个未分配的斜杠 8 个网络块分配给各种 RIR。 然后在 2011 年 4 月，APNIC 的地址用完。 成熟是下一个，在 2012 年 9 月。 2014 年 6 月，LANIC 用完了要分配的地址。 而阿林在 2015 年 9 月也做了同样的事情。 只有非洲网络中心还剩下一些 IP，但预计到 2018 年将耗尽这些 IP。维基百科有一篇很棒的文章，所有关于 IPv4 耗尽和 涉及的时间表。 我在这段视频之后的阅读中添加了一个链接。 这当然是互联网的一个重大危机。 IPv6 将最终解决这些问题， 我们将在本课程后面详细介绍。 但在全球范围内实施 IPv6 需要一些时间。 目前，我们希望继续增长，我们希望更多的人和设备 连接到它，但如果没有分配 IP 地址，则需要一种解决方法。 扰流板警报，您已经知道此变通方法的主要组成部分。 NAT 和不可路由地址空间。 请记住，不可路由的地址空间是在 RFC1918 中定义的， 由几个不同的 IP 范围组成，任何人都可以使用。 而 且无限数量的网络可以在内部使用非路由地址空间， 因为 Internet 路由器不会将流量转发到它。 这意味着 当人们使用这些地址空间时，永远不会发生任何 IP 地址的全局冲突。 由 于 NAT 等技术，非路由地址空间现在很大程度上可用。 借助 NAT， 您可以拥有数百甚至数千台使用非路由地址空间的计算机。 然 而，只有一个公共 IP， 所有这些计算机仍然可以向互联网发送流量并接收来自互联网的流量。 您只需要一个 IPv4 地址，并且通过 NAT， 具有该 IP 的路由器可以代表它后面的大量计算机。 这不是一个完美的解决方案，但在 IPv6 变得更加全球可用之前， 不可路由的地址空间和 NAT 将不得不执行