## VM Abstraction: The Stack

![image-20210107104519889](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101075gt1eA.png)

### Stack machine abstraction



### Stack

![image-20210107105317270](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107timYEB.png)

Stack operations:

- Push: add a plate at the stack's top
- Pop remove the top plate

![image-20210107105554371](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107BKenWs.png)







### Stack arithmetic

![image-20210107105741001](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107DP0K7p.png)



Apply a function f on the stack:

- Pops the argument(s) from the stack
- Computes f on the argument
- Pushes the result onto the stack

![image-20210107105824589](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101078I2gEX.png)



#### Stack arithmetic (big picture)

![image-20210107110119752](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107mgWLNx.png)

Abstraction / implementation

- The high-level language is an abstraction
- It can be implemented by a stack machine
- The stack machine is an abstraction
- It can implemented by ... Stay tuned







#### The stack machine model

![image-20210107110216531](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107bPsZ4C.png)



#### Arithmetic commands

![image-20210107110542679](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107HtXZYc.png)

#### Logical commands

![image-20210107110746962](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107ouyvR3.png)





#### Arithmetic / Logical commands

![image-20210107110821365](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107hAqW9K.png)

