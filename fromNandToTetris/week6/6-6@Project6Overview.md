## Project 6 Overview 



### Developing a Hack Assembler

Contract

- Develop a HackAssembler program that translates Hack assembly programs into executable Hack binary code
- The source program is supplied in a text file named Xxx.asm
- The generated code is written into  a text file named Xxx.hack
- Assumption: Xxx.asm is error-free





Usage

Prompt> java HackAssembler Xx.asm

This command should create (or override) an Xxx.hack file that can be executed as-is on the Hack computer



### Proposed design

The assembler can be implemented in any high-level language

Proposed software architecture

- `Parser`: unpacks each instruction into its underlying fields
- `Code`: translates each field into its corresponding binary value
- `SymbolTable`: manages the symbol table
- `Main`: initializes the I/O files and drives the process





### Proposed Implementation

Staged development

- Develop a basic assembler that translates assembly programs without symbols
- Develop an ability to handle symbols 
- Morph the basic assembler into an assembler that can translate any assembly program



Supplied test programs

Add.asm

Max.asm

Rectangle.asm

Pong.asm

MaxL.asm

RectangleL.asm

PongL.asm





#### Test program: `Add`

Basic test of handling:

- White space
- Instructions



#### Test program: `Max`		 `MaxL`(without symbols)



#### Test program: `Rectangle`		`RectangleL`



#### Test program: `Pong`		`PongL`