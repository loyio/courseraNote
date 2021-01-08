## VM Translator: Proposed Implementation

### The VM translator

![image-20210108114826699](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108IvEWwW.png)



### VM translator: proposed implementation 

![image-20210108114930191](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108GitBQm.png)





### Main

Input: 

- fileName.vm : the name of a single source file, or
- directoryName: the name off a.directory containing one or more .vm source files

Output:

- fileName.asm file, or
- directoryName.asm file



Process:

- Constructs a CodeWriter
- If the input is a .vm file:
  - Construct a Parser to handle the input file
  - Marches through the input file, parsing each line and generating code from it
- If the input is a directory:
  - Handles every .vm file in the directory in the manner described above



Implementation note:

An extension of the Main program written in project 7





### Parser

- Handles the parsing of a single .vm file
- Reads a VM command, parses the command into its lexical components, and provides convenient access to these components
- Removes all white space and comments



Implementation

- Same parser that was implemented in project 7
- If your Parser does not handle the paring of the VM commands goto, `if-goto`, `label`, `call`, `function` , and `return`, add this functionality now 



### CodeWriter

API of basic CodeWriter

![image-20210108115630503](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108dwuHUi.png)





Additional functionality :

![image-20210108115743258](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108mZpvH9.png)





