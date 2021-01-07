## Input / Output



Peripheral I/O devices:

- Keyboard
- Screen



I/o devices are used for:

- Getting data from users
- Displaying data to users





### Screen memory map

A designated memory area, dedicated to manage a display unit

![Screen Shot 2021-01-04 at 11.22.53 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010418jgu5.png)



To set pixel (row, col) on/off

![Screen Shot 2021-01-04 at 11.32.51 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104AnVWz5.png)



Action

![image-20210104113803709](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104xHjM2e.png)



#### Keyboard memory map

The physical keyboard is associated with a keyboard memory map



single 16-bit register



When a key is pressed on the keyboard, the key's scan code appears in the keyboard memory map



#### The Hack character set

![Screen Shot 2021-01-04 at 11.41.23 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104YQweV9.png)



To check which key is currently pressed:

- Probe the contents of the keyboard chip
- In the Hack computer: probe the content of RAM[24576]



If the register content 0, no key is present

![image-20210104114747766](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104SDVOGd.png)

