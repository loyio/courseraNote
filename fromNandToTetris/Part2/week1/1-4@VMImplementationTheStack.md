## VM Implementation: The stack



### Pointer manipulation





![image-20210107113902501](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107FCktOs.png)

Notation:

*p // the memory location that p points at

![image-20210107114200266](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107lPuUzS.png)

x++ // increment x = x + 1

x-- //increment x = x - 1



### Stack machine



Abstraction:

![image-20210107114536822](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107yIUvlD.png)



Implementation:

Assumptions:

- SP stored in RAM[0]
- Stack base addresses = 256

![image-20210107114909077](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107RNZcHj.png)





### VM translator perspective

![image-20210107115459930](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107YLHRUp.png)

VM Translator

- A program that translates VM code into machine language
- Each VM command generates several assembly commands