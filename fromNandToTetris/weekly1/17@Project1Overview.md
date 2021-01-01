## Project 1 Overview

#### the course methodology 



#### Project 1



Given: Nand



Goal: Build the following gates;

![image-20210101095549588](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/t7vHJO.png)





#### species

![image-20210101101539740](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/YkXjKp.png)







#### Multiplexor

![Screen Shot 2021-01-01 at 10.17.47 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/K1FtFh.png)



Example: using mux logic to build a programmable gate





#### Demultiplexor

![Screen Shot 2021-01-01 at 10.21.23 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/v9Wuqc.png)





#### And16

![Screen Shot 2021-01-01 at 10.26.18 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/wMhjm7.png)





#### 16-bit,4-way multiplexor

![image-20210101102807279](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/zDCo4J.png)





#### Chip building materials(using Xor as an example)

![image-20210101102958728](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/KOmYT8.png)





#### Hack chipset API

![image-20210101103346039](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210101So532w.png)





#### Implementation end-notes

- Create and edit your `*.hdl` files using a text editor
- A chip cannot be used in its own implementation
- When running an HDL program in the hardware simulator, errors are reported in red, at the left-bottom corner
- Multi-bit busses(unit 1.6) are indexed right to left:If `A` if a 16-bit bus, then `A[0]` is the right-most bit, and `A[15]` is the left-most bit
- Use the supplied resources:
  - Hardware simulator tutorial
  - HDL Appendix(book)
  - HDL Survival Guide(by Mark Armbrust)