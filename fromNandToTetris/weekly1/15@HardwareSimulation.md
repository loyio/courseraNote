## Hardware Simulation



### Hardware simulation in a nutshell

![Screen Shot 2020-12-31 at 6.37.24 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/mUxrcu.png)



Simulation options:

- Interactive
- Script-based
- WIth / without output and compare files



### Interactive simulation(using Xor as an example)

$Xor.hdl$

```hdl
CHIP Xor{
  IN a,b;
  OUT out;
  
  PARTS:
  NOT(in=a, out=nota);
  NOT(in=b, out=notb);
  And(a=a, b=notb, out=aAndNotb);
  And(a=nota, b=b, out=notaAndb);
  Or(a=aAndNotb, b=notaAndb, out=out);
```





### Script-based simulation

$Xor.tst$

```tst
load Xor.hdl;
set a 0, set b 0,eval;
set a 0, set b 1,eval;
set a 1, set b 0,eval;
set a 1, set b 1,eval;
```





Benefits

- "Automatic" testing
- Replicable testing





![Screen Shot 2020-12-31 at 7.17.29 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/PvY8uU.png)









### Revisiting script-based simulation with output files

$Xor.hdl$

$Xor.tst$

$Xor.out$





### Script-based simulation, with compare files

$Xor.cmp$

```cmp
| a | b |out|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |
```







## Behavioral simulation

Correct chip implementation

test script





## Hardware construction projects

- The palyer(first approximation):
  - System architects
  - Developers
- The system architect decides which chips are needed
- For each chip, the architect creates
  - A chip API
  - A test script
  - A compare file
- Given these resources,the developers can build the chips.



## The developers's view

stub file

test script 

compare file