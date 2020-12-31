## Boolean Logic



### Boolean Values

- F N 0

- T Y 1





### Boolean Operation

(x AND y)

x$\land$y

  

| x    | y    | AND  |
| ---- | ---- | ---- |
| 0    | 0    | 0    |
| 0    | 1    | 0    |
| 1    | 0    | 0    |
| 1    | 1    | 1    |





(x OR y)

x$\lor$y

| x    | y    | AND  |
| ---- | ---- | ---- |
| 0    | 0    | 0    |
| 0    | 1    | 1    |
| 1    | 0    | 1    |
| 1    | 1    | 1    |





0(x)

$\lnot$x

| x    | NOT  |
| ---- | ---- |
| 0    | 1    |
| 1    | 0    |





NOT(0 OR(1 AND 1)) = NOT(0 OR 1) = NOT(1) = 0





### Boolean Functions

f(x,y,z) = (x AND y) OR (NOT(x) AND z)

![Screen Shot 2020-12-31 at 11.33.51 AM](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/f8KTFl.png)





### Boolean Identities



Commutative Laws

- (x AND y) = (y AND x)
- (x OR y) = (y OR x)



Associative Laws

- (x AND (y AND z)) = ((x AND y) AND z)
- (x OR(y OR z)) = ((x OR y) OR z)



Distributive Laws

- (x AND (y OR z)) = (x AND y) OR (x AND z)
- (x OR (y AND z)) = (x OR y) AND (x OR z)



De Morgan Laws

- NOT(x AND y) = NOT(x) OR NOT(y)
- NOT(x OR y) = NOT(x) AND NOT(y)



easy to prove this laws







### Boolean Algebra

NOT(NOT(x) AND NOT(x OR y)) = 

NOT(NOT(x) AND (NOT(x) AND NOT(y))) = 

NOT((NOT(x) AND NOT(x)) AND NOT(y)) = 

NOT(NOT(x) AND NOT(y)) = 

NOT(NOT(x)) OR NOT(NOT(y)) =

x OR y