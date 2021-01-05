## Central Processing Unit



#### The Hack CPU: Abstraction

A 16-bit processor, designed to:

- Execute the current instruction
- Figure out which instruction to execute next (instruction written in the Hack language)





#### Hack CPU Interface

![image-20210105094900666](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105KUPs9t.png)

![image-20210105095015008](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105AGBhAr.png)



#### Hack CPU Implementation

![image-20210105095152808](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101054e1ZzZ.png)



#### Instruction handling

##### A-instrcution

![Screen Shot 2021-01-05 at 9.56.46 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105Wv2Zi3.png)

##### C-instruction

![image-20210105100007325](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105a9sJRn.png)





#### ALU operation



##### input

![image-20210105100330309](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105qGt8Z4.png)

ALU data inputs:

- From the D-register
- From the A-register / M-register



ALU control inputs:

- Control bits (from the instruction)





#### outputs

![image-20210105100617354](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105XUifv7.png)

ALU data output:

- Result of ALU calculation, fed simultaneously to : D-register, A-register, M-register
- Which register actually received the incoming value is determined by the instruction's destination bits





#### Possible out side view of the Hack computer

![image-20210105100821012](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105h5UK05.png)





#### Control(abstraction)

![image-20210105101339243](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101052jL9Dr.png)

`PC` logic

```
if(reset==1) PC=0
else
	// current instruction
	load = f(jump bits, ALU control outputs)
	if(load==1)PC=A
	else PC++
```

