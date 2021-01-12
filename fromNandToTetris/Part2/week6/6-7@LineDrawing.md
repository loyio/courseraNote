## Line Drawing



![image-20210112152315188](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112YQpOU7.png)



### Circle Drawing

![image-20210112152354615](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112YnR5iV.png)

![image-20210112152421463](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101/0112p2DNC5.png)



#### drawPixel

Issues:

Uses the service of the OS Memory class:

- Memory.peek
- Memory.poke

Setting a single bit in a 16-bit value can be done using logical 16-bit operations



#### drawLine

Issues

- Modify the algorithm for a screen origin (0,0) at the screen's top-left corner
- Generalize the algorithm to draw lines that go in any direction
- Drawing horizontal and vertical lines should probably be handled as special cases



#### drawCircle

Issues

- Can potentially lead to overflow
- To handle, limit r to no greater than 181





