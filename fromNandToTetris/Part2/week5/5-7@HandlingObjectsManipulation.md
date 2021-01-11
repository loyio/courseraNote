## Handling Objects: Manipulation



### Compiling method calls

![image-20210111133518122](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0111ZckzHf.png)



### Compiling methods:

Methods are designed to operate on the current object(this):

Therefore, each method's code needs access to the object's field



How to access the object's fields:

- The method's code can access the object's i-th field by access this i
- But first, the method's code must anchor the this segment on the object's data, using `pointer`



