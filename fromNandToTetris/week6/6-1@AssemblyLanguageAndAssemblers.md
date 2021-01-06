## Assembly Language and Assemblers



### This is Software



- The "Assembler" is software

- First software layer above the hardware



Where does the Assembler Program Run



Assembly Language Program -> Assembler(Your Home PC) -> Machine Language Program -> Hack Computer



### Basic Assembler Logic 

![image-20210106092221819](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106Vw8E64.png)





##### Read the next Assembly language command

![image-20210106092302361](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106a8pEF1.png)

##### Break it into the different fields it is composed of

##### Lookup the binary code for each field

![image-20210106092503754](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106vhiKV3.png)



##### Combine these codes into a single machine language command

![image-20210106092820638](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106LPbUjI.png)

##### Output this machine language command

![image-20210106092922784](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101066xIpoE.png)





### Symbols

- Used for:
  - Labels	`JMP loop`
  - Variables  `Load R1, weight`



#### Allocation of variables

#### Labels