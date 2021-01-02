## Negative Numbers

Representing Numbers in 4 Bits

![image-20210102145454073](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102Zq7MZ0.png)



### First bits is -/+

All other bits represent a positive number





### 2's Complement

Represent Negative number $$-x$$ using the positive number: $$2^n-x$$





### Addition in 2's Complement

![image-20210102150629781](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010286ybdD.png)



### Computing $$-x$$

Input: $$x$$

Output: $$-x$$ (in 2s complement)



Idea: $$2^n - x = 1+(2^n-1)-x$$

![image-20210102151555774](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210102YywPTa.png)

Out 4