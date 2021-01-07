## Developing the Hack Assembler: Proposed Software Architecture



### Sub-tasks that need to be done

- Reading and parsing commands
- Converting mnemonics -> code
- Handling symbols



#### Reading and Parsing Commands

No need to understand the meaning of anything

- Start reading a file with a given name
- Move to the next Command in the file 
- Get the fields of the current command





#### Translating Mnemonic to Code : Overview

No need to worry about how the mnemonic fields were obtained

![image-20210106104557549](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106BwZkHV.png)



#### The Symbol Table

No need to worry about what these symbols mean

- Create an new empty table
- Add a (symbol, address) pair to the table
- Does the table contain a given symbol?
- What is the address associated with a given symbol?



#### Using the Symbol Table

- Create a new empty table
- Add all the pre-defined symbols to the table
- While reading the input, add labels and new variables to the table
  - Labels: when you see a "(xxx)" command, add "xxx" and the address of the next machine language command
  - Variables: when your see an "@xxx" command, where "xxx" is not a number and not already in the table, add "xxx" and the next free addresss for variable allocation
- Whenever you see a "@xxx" command, where xxx is not a number, consult the table to replace the symbol xxx with its address





### Overall logic

- Initialization
  - Of parser
  - Of symbol Table
- First Pass: Read all commands, only paying attention to labels and updating the symbol table
- Restart reading and translating commands
- Main Loop:
  - Get the next Assembly Language Command and parse it
  - For A-commands: Translate symbols to binary addresses
  - For C-commands: get code for each part and put them together 
  - Output the resulting machine language command 

