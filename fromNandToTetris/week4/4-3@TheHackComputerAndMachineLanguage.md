## The Hack Computer and Machine Language

#### Hack computer: hardware

![Screen Shot 2021-01-04 at 10.40.09 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104yZj1Wj.png)

A 16-bit machine consisting of:

- Data memory(RAM): a sequence of 15-bit registers
- Instruction memory(ROM): a sequence of 15-bit registers
- Central  Processing Unit
- Instruction bus /data bus / address buses







#### Hack computer: software

![Screen Shot 2021-01-04 at 10.42.14 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104MiZdbM.png)

Hack machine language:

- 16-bit A-instructions
- 16-bit C-instructions



Hack program = sequence of instructions written in the Hack machine language





#### Hack computer: control

![Screen Shot 2021-01-04 at 10.43.49 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104n888Yp.png)

- The ROM is loaded with a Hack program
- The reset button is pushed
- The program start running





#### Hack computer: registers

![Screen Shot 2021-01-04 at 10.45.49 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104sdgmym.png)

The Hack machine language recognizes three registers:

- D hold a 16-bit value
- A hold a 16-bit value
- M represents the 16-bit RAM register addressed by A





#### The A-instruction

Syntax: @value

Where value is either:

- a non-negative decimal constant or
- a symbol referring to such a constant(later)



Semantics:

- Sets the A register to value
- Side effect: RAM[A] becomes the selected RAM register



#### The C-instruction

`dest = comp; jump` (both dest and jump are optional)

![Screen Shot 2021-01-04 at 10.54.16 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210104G9I62C.png)

