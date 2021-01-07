## Hack Programing Part 2



### Branching

example:

```basic
// Program: Signum.asm
// Cpmputes: if R0>0
//							R1=1
//           else
//   	 					R1=0
  
  @R0
  D=M
  
  @POSITIVE
  D;JGT
  
  @R1
  M=0
  @END
  0;JMP

(POSITIVE)
  @R1
  M=1

(END)  
  @10
  0;JMP       
```

(POSITIVE): declaring a label

@POSITIVE: using a label





### Variables

variable usage example:

```basic
// Program: Flip.asm
// flips the value of RAM[0] and RAM[1]

// temp=R1
// R1 = R0
// R0 = temp


@R1
D=M
@temp
M=D

@R0
D=M
@R1
M=D

@temp
D=M
@R0
M=D

(END)
@END
0;JMP
```

@temp: each occurrence of @temp in the program will be translated into @n





### Iterative processing

Example:

Compute 1+2+..+n

![image-20210104124345640](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104ZbYY2p.png)

Tracing the program's execution



Best practice:

1. Design the program using pseudo code
2. Write the program in assembly language
3. Test the program(on paper) using a variable-value trace table