## Developing Apps using the Jack language and OS



Put all the app files in one directory, whose name is the app name

<u>Write / edit</u> your Jack class files using a standard text editor

<u>Compile</u> your Jack files / directory using the supplied `JackCompiler`

<u>Execute</u> your app by loading the app directory (which now contains the compiled .vm files) into the supplied VM Emulator, and running the code





### Handling output: text

Textual apps:

- Screen: 23 rows of 64 character, b&w
- Font: features by the Jack OS
- Output: Jake OS output class

![image-20210109112507761](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109udkamg.png)





### Handling output: graphics

Graphical apps:

- Screen: 256 rows of 512 pixels, b&w
- Output: Jack OS Screen class (or do your own)

![image-20210109112608494](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109sRxn8i.png)





Handling inputs

Input device:

- Standard keyboard
- Input programming : use the OS keyboard class

![image-20210109112717473](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109RvzDHw.png)



The Jack character set

![image-20210109112737432](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109DanteV.png)





### Keyboard.keypress()

Returns the code of the currently pressed key, or 0 when no key is pressed



### The Jack OS: `Math`

![image-20210109112844759](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109pmulJs.png)



### The Jack OS: String

![image-20210109113003639](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109SX2xBu.png)



### The Jack OS: Array

![image-20210109113034899](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109iMUCA6.png)



### The Jack OS: `Memory`

![image-20210109113115378](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109VtngRQ.png)





### The Jack OS: `Sys`

![image-20210109113159155](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109YW266h.png)



### The Jack OS: `Keyboard`

![image-20210109113306334](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109SUARhT.png)





### Sample Jack programs

- All the programs shown throughout this module
- Square: a simple, interactive, multi-class OO application
- Pong: a complete, interactive, multi-classs OO application
- Average: illustrates simple array processing
- ComplexArrays: illustrates various array manipulations, including two-dimentsional arrays 
- ConvertToBin: illustrates algebraic operations, and working with peek and poke







### Best practice



![image-20210109113545732](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210109RvzMzj.png)