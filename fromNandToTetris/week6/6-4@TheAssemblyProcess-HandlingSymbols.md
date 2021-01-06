## The Assembly Process - Handling Symbols



### Symbols

- Variable symbols: represent memory locations where the programmer wants to maintain values
- Label symbols: represent destinations of goto instructions 
- Pre-definded symbols: represent special memory locations





### Handling pre-defined symbols

The hack language specification describes 23 pre-defined symbols:

![image-20210106101130822](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106urLlVj.png)



### Handling symbols that denote labels

Label symbols

- Used to label destinations of goto commands
- Declared by the pseudo-command (XXX)
- This directive defines the symbol XXX to refer to the memory location holding the next instruction in the program

![image-20210106101452188](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106qxr4tH.png)





### Handling symbols that denote variables

Variable symbols

- Any symbol XXX appearing in an assembly program which is not pre-defined and is not defined elsewhere using the (XXX) directive is treated as a _variable_
- Each variable is assigned a unique memory address, starting at 16

![image-20210106101742589](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106uf8POm.png)

#### Symbol table

![image-20210106102627454](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210106wAU4zL.png)

First pass: add the label symbols

Second pass: Add the var. symbols



Usage:

To resolve a symbol, look up its value in the symbol table





### The assembly process

Initialization:

- Construct an empty symbol table 
- Add the pre-defined symbols to the symbol table



First Pass:

Scan the entire program;

For each "instruction" of the form (XXX):

- Add the pair (XXX, address) to the symbol table, where address is the number of the instruction following (XXX)



Second pass:
Set $$n$$ to 16

Scan the entire program again; for each instruction:

- If the instruction is @symbol, look up symbol in the symbol table;
  - If (symbol, value) is found, use value to complete the instruction's translation;
  - If not found:
    - Add (symbol, n) to the symbol table,
    - Use n to complete the instruction's translation,
    - n++
  - If the instruction is a C-instruction, complete the instruction's translation
  - Write the translated instruction to the output file



