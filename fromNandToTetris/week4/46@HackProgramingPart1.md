## Hack Programing Part 1

#### Hack assembler

Assembly program to Binary code





#### CPU Emulator

Assembly program translate and load to CPU Emulator





#### Hack programing

- Working with registers and memory
- Branching
- Variables
- Iteration
- Pointers
- Input / ouput



##### Working with registers and memory

D: data register

A: address / data register

M: the currently selected memory register, M = RAM[A]



Typical operations:

```basic
// D=10
@10
D=1

//D++
D=D+1

// D=RAM[17]
@17
D=M

// RAM[17]=D
@17
M=0

// RAM[17]=10
@10
D=A
@17
M=D

// RAM[5] = RAM[3]
@3
D=M
@5
M=D
```



Hack program example: add two numbers

```basic
// program: add2.asm
// computes: RAM[2] = RAM[0] + RAM[1]
// Usage: put values in RAM[0], RAM[1]

@0
D=M // D=RAM[0]

@1
D=D+M // D=D+RAM[1]

@2
M=D //RAM[2]=D
```

Action

![image-20210104121235702](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104Czj4A3.png)



Best practice:

to terminate a program safety, en it with an infinite loop

```basic
@6
0;JMP
```





#### Built-in symbols

The Hack assembly language features built-in symbols:

![Screen Shot 2021-01-04 at 12.17.02 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101049aOBfI.png)

![Screen Shot 2021-01-04 at 12.19.21 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104AUYs7p.png)



>  Hack is case-sensitive: R5 and r5 are different

Screen and KBD: base addresses of I/O memory maps

Remaining symbols: used in the implementation of the Hack virtual machine discussed in Nand to Tetris Part II

![Screen Shot 2021-01-04 at 12.21.17 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104i1V1KW.png)

