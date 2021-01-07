## Boolean Function Synthesis



Boolean Expression -> Truth table

Truth Table -> Boolean Expression



### Truth Table to Boolean Expression

![Screen Shot 2020-12-31 at 11.48.01 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/PUhhOS.png)





#### Theorem



Any Boolean fucntion can be represented using an expression containing  AND and NOT operations.



Proof:

(x OR y) = NOT(NOT(x) AND NOT(y))









### NAND

| x    | y    | NAND |
| ---- | ---- | ---- |
| 0    | 0    | 1    |
| 0    | 1    | 1    |
| 1    | 0    | 1    |
| 1    | 1    | 0    |



(x NAND y) = NOT(x AND y)





#### Theorem

Any Boolean function can be represented using an expression containing only NAND operations



Proof:

1) NOT(x) = (x NAND x)

2) (x AND y) = NOT(x NAND y)