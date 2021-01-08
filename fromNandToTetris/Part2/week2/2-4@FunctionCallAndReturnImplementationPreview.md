## Function Call and Return: Implementation Preview



### Function execution

- A computer program typically consists of many functions
- During a given point of time, only a few functions are executing
- Calling chain: `foo` > `bar` > `sqrt` > ...





### The function's state

![image-20210108100807824](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101087GNrg3.png)



![image-20210108101023050](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010844FHI0.png)



### Function call and return:  the big picture

Example: computing mult(17,212)

![image-20210108101140453](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101084g9zFc.png)



#### The details 

##### call

![image-20210108101447958](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108uwCcg2.png)





##### function 

![image-20210108101719436](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108Su0daO.png)





##### return

![image-20210108101903059](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108mK2gga.png)





##### The caller resumes the  execution



### The global stack

![image-20210108102613407](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010837JOKV.png)



Recap:

![image-20210108102807064](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108ktcWOJ.png)

