## Jack Language Specification: Methods



### Subroutines

#### Subroutine declaration

![image-20210109110154245](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010944DqC3.png)



Jack subroutines

- Constructors: create new objects
- Methods: operate on the current object
- Functions: static methods



Subroutine types and return values

- Method and functions type can be either void, a primitive dat type, or a class name
- Each subroutine must return a value

Constructors

- 0,1 or more in a class
- Common name: new
- The constructor's type must be the name of the constructors class
- The constructor must return a reference to an object of the class type



Variables

Variable kinds:

- *static* variables
- *field* variables
- *local* variables
- *parameter* variables

Variables must be :

- Declared before they are used
- Typed



### Variables

![image-20210109110548728](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109sAoTMI.png)





### Statements

![image-20210109110627636](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010999OuOC.png)







### Expressions

A Jack expression is one of following:

- A constant
- A variable name in scope, The variable may be static, field, local, or parameter
- The this keyword, denoting the current object (cannot be used in functions)
- An array element using the syntax Arr[expression], where Arr is a variable name of type Array in scope

![image-20210109110822657](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101093Vq8r4.png)







Subroutine calls

Examples:

![image-20210109110848975](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010959Ub21.png)



![image-20210109110914386](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109XUcGby.png)





### Strings

Examples

![image-20210109111241313](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109GR6suE.png)





### Arrays

Examples:

![image-20210109111505067](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109HPoDUm.png)

Jack array are  ...

- Instances (objects) of the OS class Array
- Not typed
- Uni-dimenstional
- Multi-dimensional array can be obtained by using a arrays of arrays





End note: peculiar features of the Jack language

![image-20210109111628223](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101095e5H14.png)