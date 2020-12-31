## Hardware Simulation



### Hardware simulation in a nutshell

![Screen Shot 2020-12-31 at 6.37.24 PM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/mUxrcu.png)



Simulation options:

- Interactive
- Script-based
- WIth / without output and compare files



### Interactive simulation(using Xor as an example)

$Xor.hdl$

```basic
CHIP Xor{
  IN a,b;
  OUT out;
  
  PARTS:
  NOT(in=a, out=nota);
  NOT(in=b, out=notb);
  And(a=a, b=notb, out=aAndNotb);
  And(a=nota, b=b, out=notaAndb);
  Or(a=aAndNotb, b=notaAndb, out=out);
}
```

