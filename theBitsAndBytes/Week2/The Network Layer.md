## The Network Layer

ARP : Address Resolution Protocol



### IP Addresses

32-bit 

IP addresses belong to networks, not to the devices attached to those networks



- Dynamic IP address

- Static IP address



In most cases, static IP addresses are reserved for servers and network devices, while dynamic IP addresses are reserved for clients





### IP Datagrams and Encapsulation



IP datagram

A highly structured series of fields that are strictly defined 

![image-20210106200945308](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106CHlodx.png)



The most common version of IP is version 4, or IPv4



#### Header Length field

Almost always 20 bytes in length when dealing with IPv4



#### Service Type field

These 8 bits can be used to specify details about quality of service, or QoS, technologies



#### Total Length

Indicates the total length of the IP datagram It's attached to 



#### Identification

A 16-bit number that's used to group messages together 



The maximum size of a single datagram is the largest number your can represent with 16 bits 65535

If the total amount of data that needs to be sent is larger than what can fit in a single datagram, the IP layer needs to split this data up into many individual packets



#### Flag field 

Used to indicate if a datagram is allowed to be fragmented, or to indicate that the data gram has already been fragmented 



#### Fragmentation

The process of taking a single IP datagram and splitting it up into several smaller datagrams



#### Time to Live(TTL) field

An 8-bit field that indicates how many router hops a datagram can traverse before it's thrown away



#### Protocol field

Another 8-bit field that contains data about what transport layer protocol is being used

- TCP
- UDP



#### Header checksum field

A checksum of the contents of the entire IP datagram header



#### Source IP address

#### Destination IP address



#### IP options field

An optional field and is used to set special characteristics for datagrams primarily used for testing purposes



#### Padding field

A series of zeros used to ensure the header is the correct total size





### IP address Classes

IP addresses can be split into two sections: the network ID and the host ID

![Screen Shot 2021-01-06 at 8.25.22 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106qU9B10.png)

#### Address class system

A way of defining how the global IP address space is split up 

- Class A : first 
- Class B: first two octets are used for the network ID
- Class C: first three octets and used for the network ID

![image-20210106203340385](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106IZzDOc.png)





#### CIDR

Classless Inter-Domain Routing



#### Address Resolution Protocol

a protocol used to discover the hardware address of a node with a certain 

IP address



#### APR Table

a list of IP addresses an the Mac addresses associated 

with them



ARP table entries generally expire after a short amount of time to ensure changes in 

the network are accounted for 