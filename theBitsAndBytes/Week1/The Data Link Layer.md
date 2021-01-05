## The Data Link Layer



### Ethernet and MAC Addresses



#### collision domain

Ethernet as a protocol solved this problem by using a technique known as carrier sense multiple access with collision detection



#### CSMA/CD

Used to determine when the communications channels are clear, and when a device is free to transmit data 



#### MAC address

A globally unique identifier attached to an individual network interface 

It's a 48-bit number normally represented by six groupings of two hexadecimal numbers



#### Octet

In computer networking, any number that can be represented by 8 bits





#### Organizationally Unique Identifier(OUI)

The first three octets of a MAC address





Ethernet uses MAC addresses to ensure that the data it sends has both an address for the machine that sent the transmission, as well as the one the transmission was intended for.





### Unicast, Multicast, and Broadcast



##### A unicast transmission is always meant for just one receiving address 



##### If the least significant bit in the first octet of a destination address is set to zero, it means that ethernet frame is intended for only the destination address

##### If the least significant bit in the first octet of a destination address is set to one, it means you're dealing with a multicast frame 



##### Broadcast

![image-20210105204605062](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105joAkKj.png)



### Dissecting an Ethernet Frame



#### Data packet

An all-encompassing term that represents any single set of binary data being sent across a network link



#### Ethernet frame

![image-20210105205824538](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010523FeX4.png)

A highly structured collection of information presented in a specific order

- Preamble: 8 bytes(or 64 bit) long, and can itself be split into two sections
- Start frame delimiter(SFD): Signals to a receiving device that the preamble is over and that the actual frame contents will now follow
- Destination MAC address: The Hardware address of the intended recipient
- Source Address
- EtherType field: 16 bit long and used to describe the protocol of the content of the frame
- VLAN header: Indicates that the frame itself is what's called a VLAN frame (If a VLAN header is present, the EtherType field follows it)
- Virtual LAN (VLAN): A technique that lets you have multiple logical LANS operating on the same physical equipment
- Payload: In networking terms, is the actual data being transported, which is everything that isn't a header 
- Frame Check Sequence: A 4-byte (or 32-bit) number that represents a checksum value for the entire frame (This checksum value is calculated by performing what's known as a cyclical redundancy check against the frame)
- Cyclical Redundancy Check (CRC): An important concept for data integrity, and is used all over computing, not just network transmissions

