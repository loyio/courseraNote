## The Assembly Process - Handling Instructions



### Translating A-instructions



Translation to binary:

- If value is a decimal constant, generate the equivalent 15-bit binary constant
- If value is a symbol, later



### Translating C-instructions

Example: 

Symbolic: `MD=D+1`

Binary: `111 0 011111 011 000`



### The overall assembly logic 

For each instruction

- Parse the instruction: break it into its underlying fields
- A-instruction: translate the decimal value into a binary value
- C-instruction: for each field in the instruction, generate the corresponding binary code; Assemble the translated binary codes into a complete 16-bit machine instruction
- Write the 16-bit instruction to the output file