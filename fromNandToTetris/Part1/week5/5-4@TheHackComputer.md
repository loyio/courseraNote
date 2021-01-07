## The Hack Computer



#### Hack CPU Operation

The CPU executes the instruction according to the Hack language specification:

- If the instruction includes D and A, the respective values are read from, and/or written to, the CPU-resident D-register and A-register
- If the instruction is @x, then x is stored in the A-register; this value is emitted by addressM
- If the instruction's RHS includes M, this value is read from inM
- If the instruction's LHS include M, then the ALU output is emitted by outM, and the writeM bit is asserted



![image-20210105102550558](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105fPhq0T.png)



#### Memory

![image-20210105102647078](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105jzd3C3.png)



#### RAM

![image-20210105102844087](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105Ne4jCS.png)

#### Screen implementation

![image-20210105103110400](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105fgKn9f.png)



#### Keyboard memory map

![image-20210105103204129](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105kZBDWR.png)

##### Keyboard implementation

![image-20210105103340844](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105eFiGO9.png)



To read the keyboard:

- Probe the output of the keyboard register
- In the Hack Memory context: probe memory register 24576





### Instruction Memory(ROM)

To run a program on the Hack computer:

- Load the program into the ROM
- Press "reset"
- The program starts running



##### Loading a program

- Hardware implementation: plug-and-play ROM chips
- Hardware simulation:programs are started in text file; program loading is emulated by the built-in ROM chip





##### Action

![image-20210105103916018](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105zXRJKQ.png)





### Hack Computer implementation

![Screen Shot 2021-01-05 at 10.48.13 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105EnOiJ0.png)

