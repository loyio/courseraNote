## VM Implementation: Memory Segments



### Implementation `local`

![image-20210107115928124](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107tabLKX.png)

![image-20210107120229130](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107aLI27s.png)

![image-20210107120314711](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107ts2HhP.png)



### summary

![image-20210107120349780](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107zji6Gh.png)





### Implementing `local` , `argument` , `this`, `that`

When translating the high-level code of some method into VM code, the compilation

![image-20210107120558290](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107Byrp3m.png)



![image-20210107120727548](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101076Q3JyD.png)

Local, argument, this and that are implemented precisely the same way

![image-20210107120746373](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107NATxHV.png)





### Implementing constant

![image-20210107120941221](/Users/loyio/Library/Application Support/typora-user-images/image-20210107120941221.png)





### Implementing `static`

![image-20210107121543920](/Users/loyio/Library/Application Support/typora-user-images/image-20210107121543920.png)





### Implementing `temp`

![image-20210107121959035](/Users/loyio/Library/Application Support/typora-user-images/image-20210107121959035.png)



### Implementing `pointer`

![image-20210107122311189](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107cTbG0t.png)



### VM language

