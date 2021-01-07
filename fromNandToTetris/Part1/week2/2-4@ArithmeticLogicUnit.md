## Arithmetic Logic Unit

#### Von Neumann Architecture

![image-20210102152101958](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102QHGE3Q.png)



#### The Arithmetic Logic Unit

![image-20210102152207954](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102xYrogM.png)



#### The Hack ALU

![image-20210102152421972](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101028eNRAu.png)

Also output two 1-bit values





Control bit

![image-20210102152607739](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102wE4du9.png)



#### The Hack ALU in action: compute $$y-x$$

#### The Hack ALU in action: compute $$x \& y$$





#### The Hack ALU operation

![image-20210102153217342](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102iXBtJc.png)

##### Example

![image-20210102153600884](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101029U2k77.png)





#### The Hack ALU output control bits

![image-20210102154105942](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102Sc6sc8.png)



#### Perspective

The Hack ALU is:

- Simple
- Elegant
- Easy to implement:
  - Set a 16-bit value to 0000000000000000
  - Set a 16-bit value to 1111111111111111
  - Negate a 16-bit value(bit-wise)
  - Compute + or & on two 16-bit values
  - That's it!