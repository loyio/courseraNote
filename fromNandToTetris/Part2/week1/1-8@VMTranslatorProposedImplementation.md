## VM Translator: Proposed Implementation

### The VM translator 

![image-20210107131448213](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/2021010777HD7i.png)





### usage

`Java VMTransloator myProg.vm`



### Implementation 

Proposed design:

- Parser: parses each VM command into its lexical elements
- CodeWriter: writes the assembly code that implements the parsed command
- Main: drives the process (VMTranslator)



Main(VMTranslator)

Input: fileName.vm

Output: fielName:asm





Main logic:

- Constructs a Parser to handle the input file
- Constructs a CodeWriter to handle the output file
- Marches through the input file , parsing each line and generation code from it



### Parser

- Handles the parsing of a single .vm file
- Reads a VM command, parses the command into its lexical components ,and provides convenient access to these components 
- Ignore all white space and comments 

![image-20210107132305183](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107HZmoTx.png)





### CodeWriter

Generate assembly code from the the parsed VM command:

![image-20210107132448380](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107MYnZor.png)

