## Jack Language Specification: Classes

- Class = basic compilation unit
- Each class Foo is stored in a separate Foo.jack file
- The class name's first character must be an uppercase letter

![image-20210109104711367](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101096SrJog.png)



### Classes that provide functionality

![image-20210109104814567](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109OLfttC.png)

- Contains functions only
- (No fields, constructors, or methods)
- Offers a "library of service"



### Classes that represent entities (objects)

![image-20210109105207503](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109Z9h8Gr.png)

Best practice:

Don't mix library functionality and object  in the representation same class





### Jack application

![image-20210109105615015](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109uVQS5K.png)





### Jack's standard class library / OS

OS purpose:

- Closes gaps between high-level programs and the host hardware
- Provides efficient implementations of commonly-used functions
- Provides efficient implementations of commonly-used ADTs

OS implementation:

-  A collection of classes

- Similar to Java's standard class library







Jack's standard class library 

![image-20210109110005463](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109tj62HY.png)