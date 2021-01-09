## Why do we need DNS?



Computers speak to each other in numbers. At the very lowest levels, all computers really understand are 1 and 0. Reading binary numbers isn't the easiest for humans, so most binary numbers are represented in lots of different forms. This is especially true in the realm of networking. Remember that an IP address is really just a 32-bit binary number, but it's normally written out as 4 octets in decimal form since that's easier for humans to read. You might also remember that MAC addresses are just 48-bit binary numbers that are normally written out in 6 groupings of 2 hexadecimal digits each. While remembering 192.168.1.100 might be easier than remembering a long string of 1s and 0s, It still doesn't do a very good job when you have to remember more than just a few addresses. Imagine having to remember the four octets of an IP address for every website you visit. It's just not a thing that the human brain is normally good at. Humans are much better at remembering words. That's where DNS, or domain name system, comes into play. DNS is a global and highly distributed network service that resolves strings of letters into IP address for you. Let's say you wanted to check a weather website to see what the temperature is going to be like. It's much easier to type www.weather.com into a web browser than it is to remember that one of the IP adresses for this site is 184.29.131.121. The IP address for a domain name can also change all the time for a lot of different reasons. A domain name is just the term we use for something that can be resolved by DNS. In the example we just used, www.weather.com would be the domain name, and the IP it resolves to could change, depending on a variety of factors. Let's say that weather.com was moving their web server to a new data center. Maybe they signed a new contract, or the old data center was shutting down. By using DNS, an organization can just change what IP a domain name resolves to, and the end user would never even know. So, not only does DNS make it easier for humans to remember how to get to a website, It also lets administrative changes happen behind the scenes without an end user having to change their behavior. Try to imagine a world where you'd have to remember every IP for every website you visit, while also having to memorize new ones if something changed. We'd spend our whole day memorizing numbers. The importance of DNS for how the Internet operates, today, can't be overstated. IP addresses might resolve to different things depending on where in the world you are. While most Internet communications travel at the speed of light, the further you have to route data, the slower things will become. In almost all situations, it's going to be quicker to transmit a certain amount of data between places that are geographically close to each other. If you're a global web company, you'd want people from all over the world to have a great experience accessing your website. So instead of keeping all of your web servers in one place, you could distribute them across data centers across the globe. This way, someone in New York, visiting a website, might get served by a web server close to New York, while someone in New Delhi might get served by a web server closer to New Delhi. Again, DNS helps provide this functionality. Because of its global structure, DNS lets organizations decide, if you're in the region, resolve the domain name to this IP. If you're in this other region, resolve this domain to this other IP. DNS serves lots of purposes and might be one of the most important technologies to understand, as an IT support specialist, so you can effectively troubleshoot networking issues.



计算机互相说话的数字。 在最低级别，所有计算机真正理解为 1 和 0。 读取二进制数对人类来说并不是 最简单的，所以大多数二进制数都以很多不同的形式表示。 在网络领域尤其如此。 请记住，IP 地址实际上只是一个 32 位二进制数，但它通常以十进制 形式写出 4 个八进制字节，因为这对人类来说更容易阅读。 您可能还记得，MAC 地址只是 48 位二进制 数字，通常以 6 组 2 个十六进制数字编写。 虽然记住 192.168.1.100 可能 比记住 1 和 0 的长字符串更容易，但 当你必须记住更多的地址时，它仍然没有做一个很好的工作。 想象一下，必须记住 您访问的每个网站的 IP 地址的四个八位数。 这只是不是人类大脑通常擅长的事情。人类更好地记住话语。 这就是 DNS 或域名系统发挥作用的地方。 DNS 是一种高度分布的全球 网络服务，可将字母串解析为 IP 地址。 假设您想查看一个天气网站，看看温度 将会是什么样的。 在网络 浏览器中输入 www.weather.com 要容易得多，而不是记住 这个网站的 IP 地址之一是 184.29.131.121。 由 于 很多不同的原因，域名的 IP 地址也可以随时更改。 域名只是我们用来表示 DNS 可以解析的东西的术语。 在我们刚才使用的示例中，www.weather.com 将是域名， 而它解析的 IP 可能会根据各种因素发生变化。 假设 weather.com 正在将他们的 Web 服务器迁移到一个新的数据中心。也许他们签了新合同，或者旧的数据中心正在关闭。 通过使用 DNS，组织可以改变域名解析的 IP， 最终用户甚至永远不会知道。 因此，DNS 不仅使人们更容易记住如何访问 网站，它还允许管理更改在幕后发生， 而无需最终用户改变他们的行为。 试着想象一个世界，你必须记住 你访问的每个网站的每个 IP，同时还必须记住新的 IP，如果有什么变化。 我们会花一整天的时间记忆数字。 DNS 对于互联网运作方式的重要性如今无论怎么强调都不为过。IP 地址可能会解析为不同的内容，具体取决于 您在世界上的位置。 虽然大多数互联网通信 都以光速传输，但路由数据越远，事情就会变得越慢。 几乎在所有情况下，在地理上相互 接近的地点之间传输一定数量的数据都会更快。 如果您是一家全球性的网络公司，您希望来自世界各地的人们能够在 访问您的网站时获得极好的体验。 因此，您 可以将所有 Web 服务器保存在一个位置，而不是将它们分发到全球各地的数据中心。 这样，在纽约访问某个网站的人 可能会得到纽约附近的网络服务器的服务，而新德里的某人 可能会得到更靠近新德里的网络服务器的服务。 同样，DNS 有助于提供此功能。 由于 DNS 的全局结构，组织可以决定（ 如果您在该区域）将域名解析为此 IP。 如果您在此其他区域，请将此域解析为此其他 IP。作为 IT 支持专家，DNS 有很多用途，可能是需要理解的最重要技术之一，因此 您可以有效地解决网络问题。