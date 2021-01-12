## Project 12 : Building the OS



### OS implementation

![image-20210112155049568](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112uUo6vJ.png)





### Reverse engineering

Suppose you wish to implement an existing OS

The OS consist of n executable modules, with high inter-dependency



Strategy

For each module in the OS, implement the module separately, using the remaining n-1 executable modules to service it



Example

![image-20210112155321612](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112T9slOD.png)





### Step-wide development

![image-20210112155418926](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112q7ZxcW.png)

