## Introduction to Wireless Networking Technologies



In today's world, fewer and fewer devices are weighed down by physical cables in order to connect to computer networks. With so many portable computing devices in use, from laptops to tablets to smartphones, we've also seen the rise of wireless networking. Wireless networking, is exactly what it sounds like. A way to network without wires. By the end of this lesson, you'll be able to describe the basics of how wireless communication works. You'll know how to tell the difference between infrastructure networks, and ad hoc networks. You'll be able to explain how wireless channels help wireless networks operate. And you'll understand the basics of wireless security protocols. These are all invaluable skills as an IT support specialist, since wireless networks are becoming more and more common in the workplace. The most common specifications for how wireless networking devices should communicate, are defined by the IEEE 802.11 standards. This set of specifications, also called the 802.11 family, make up the set of technologies we call WiFi. Wireless networking devices communicate with each other through radiowaves. Different 802.11 standards generally use the same basic protocol, but might operate at different frequency bands. A frequency band is a certain section of the radio spectrum that's been agreed upon to be used for certain communications. In North America, FM radio transmissions operate between 88 and 108 megahertz. This specific frequency band is called the FM broadcast band. WiFi networks operate on a few different frequency bands. Most commonly, the 2.4 gigahertz and 5 gigahertz bands. There are lots of 802.11 specifications including some that exist just experimentally or for testing. The most common specifications you might run into are 802.11b, 802.11a, 802.11g, 802.11n, and 802.11ac. We won't go into detail about each one here. For now, just know that we've listed these in the order they were adopted. Each newer version of the 802.11 specifications has generally seen some improvement, whether it's higher access speeds, or the ability for more devices to use the network simultaneously. In terms of our networking model, you should think of 802.11 protocols as defining how we operate at both the physical and the data link layers. An 802.11 frame has a number of fields. The first is called the frame control field. This field is 16 bits long, and contains a number of sub-fields that are used to describe how the frame itself should be processed. This includes things like what version of the 802.11 was used. The next field is called a duration field. It specifies how long the total frame is. So, the receiver knows how long it should expect to have to listen to the transmission. After this, are four address fields. Let's take a moment to talk about why there are four instead of the normal two. We'll discuss different types of wireless network architectures in more detail later in this lesson, but the most common setup includes devices called access points. A wireless access point is a device that bridges the wireless and wired portions of a network. A single wireless network might have lots of different access points to cover a large area. Devices on a wireless network will associate with a certain access point. This is usually the one they're physically closest to. But, it can also be determined by all sorts of other things like general signal strength, and wireless interference. Associations isn't just important for the wireless device to talk to a specific access point, it also allows for incoming transmissions to the wireless device to be sent by the right access point. There are four address fields, because there needs to be room to indicate which wireless access point should be processing the frame. So, we'd have our normal source address field, which would represent the MAC address of the sending device. But, we'd also have the intended destination on the network, along with a receiving address and a transmitter address. The receiver address would be the MAC address of the access point that should receive the frame, and the transmitter address would be the MAC address of whatever has just transmitted the frame. In lots of situations, the destination and receiver address might be the same. Usually, the source and transmitter addresses are also the same. But, depending on exactly how a specific wireless network has been architected, this won't always be the case. Sometimes, wireless access points will relay these frames from one another. Since all addresses in an 802.11 frame are Mac addresses, each of those four fields is 6 bytes long. In between the third and fourth address fields, you'll find the sequence control field. The sequence control field is 16 bits long and mainly contains a sequence number used to keep track of ordering the frames. After this is the data payload section which has all of the data of the protocols further up the stack. Finally, we have a frame check sequence field which contains a checksum used for a cyclical redundancy check. Just like how ethernet does it.



在当今世界， 为了连接到计算机网络，通过物理电缆对设备进行称重的越来越少。 随着便携式计算设备的使用， 从笔记本电脑到平板电脑，再到智能手机， 我们也看到无线网络的兴起。 无线网络，正是它的声音。 一种无线网络的方式。 在 本课程结束时， 您将能够描述无线通信工作原理的基础知识。 您将知道如何区分 基础架构网络和点对点网络之间的区别。 您将能够解释无线通道如何帮助无线网络运行。 您将了解无线安全协议的基础知识。 作 为 IT 支持专家，这些都是非常宝贵的技能， 因为无线网络在工作场所越来越普遍。 无线网络设备应如何通信的最常见规格 由 IEEE 802.11 标准定义。 这套规格 也称为 802.11 系列，构 成了我们称之为 WiFi 的一套技术。 无线网络设备通过无线电波相互通信。 不同的 802.11 标准通常使用相同的基本协议， 但可能在不同的频段下工作。 频带是 指已商定用于某些通信的无线电频谱的某一部分。 在北美，调频无线电传输运行在 88 至 108 兆赫之间。 这个特定的频带称为 FM 广播频带。 WiFi 网络在几个不同的频带上运行。 最常见的是 2.4 千兆赫和 5 千兆赫频段。 有很多 802.11 规范， 包括一些只是实验性或测试存在的规范。 您可能遇到的最常见规格是 802.11b、 802.11a、802.11 克、802.11 克、802.11g 和 802.11g。 我们不会详细讨论每一个。 现在，只要知道我们已经按照它们被采用的顺序列出了这些。 802.11 规范的每个新版本通常都有一些改进， 无论是访问速度更高， 还是能够让更多设备同时使用网络。 就我 们的网络模型而言， 您应该将 802.11 协议视为 我们在物理层和数据链路层的运作方式。 802.11 帧有许多字段。 第一个称为帧控制字段。 此字段长度为 16 位 ，包含许多子字段，用于 描述如何处理帧本身。 这包括使用的是什么版本的 802.11。 下一个字段称为持续时间字段。 它指定总帧的长度。 所以，接收器知道它应该期待多长时间不得不听传输。 在此之后, 有四个地址字段. 让我们花点时间来谈谈为什么有四个而不是正常的两个。 我们将在 本课后面更详细地讨论不同类型的无线网络架构， 但最常见的设置包括称为接入点的设备。 无线接入点是一种 连接网络无线和有线部分的设备。 单个无线网络可能有 很多不同的接入点来覆盖大面积。 无线网络上的设备将与特定接入点关联。 这通常是他们身体上最接近的一个。 但是，它也可以通过各种其他因素来确定， 如一般信号强度和无线干扰。 关联不仅对于 无线设备与 特定接入点 通信非常重要，还允许通过正确的接入点将传入到无线设备的传入传输。 有四个地址字段， 因为需要有空间来指示 哪个无线接入点应该处理帧。 因此，我们将有我们的普通源地址字段， 它将表示发送设备的 MAC 地址。 但是，我们也会在网络上拥有预期目的地 ，以及接收地址和发射机地址。 接收机地址将是接 收帧的接入点的 MAC 地址 ，发射机地址将 是刚传输帧的 MAC 地址。 在许多情况下， 目的地址和接收方地址可能相同。 通常，源地址和发射机地址也相同。 但是，根据特定无线网络的构建方式， 情况并非总是如此。 有时，无线接入点会相互中继这些帧。 由于 802.11 帧中的所有地址都是 Mac 地址，因此 这四个字段中的每个字段都有 6 个字节的长度。 在第三个和第四个地址字段之间， 您将找到序列控制字段。 序列控制字段长度为 16 位，主要 包含用于跟踪帧排序的序列号。 之后是数据 有效负载部分，其中包含堆栈上方协议的所有数据。 最后，我们有一个帧校验序列字段 ，其中包含用于周期冗余检查的校验和。 就像以太网一样。