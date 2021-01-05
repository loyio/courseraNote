## The Fetch-Execute Cycle

The basic CPU loop

- Fetch an Instruction from the Program memory
- Execute it





#### Fetching

- Put the location of the next instruction into the "address" of the program memory
- Get the instruction code itself by reading the memory contents at that location



#### The Program Counter

![image-20210105093724639](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105uV739z.png)



#### Executing

- The instruction code specifies "what to do"
- Ofter, different subsets of the bits control different aspects of the operation
- Executing the operation involves also accessing registers and/or data memory



#### Executing an Instruction



#### Fetch-Execute Clash

![image-20210105094121501](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105Rff1wo.png)



#### Solution: Multiplex

![image-20210105094221190](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210105oS8BUs.png)



#### Simple Solution: Harvard Architecture

- Variant of von Neumann Architecture
- Keep Program and Data in two separate memory modules
- Complication avoided