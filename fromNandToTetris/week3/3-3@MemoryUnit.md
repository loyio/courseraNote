## Memory Units

#### Von Neumann architecture



#### Memory

- Main memory: RAM,...
- Secondary memory: disk,...
- Volatile /not-volatile





RAM:

- Data
- Instructions



Perspective:

- Physical
- Logical









### The most basic memory element: Register

![image-20210103103621722](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210103HddZT8.png)





### Register / read logic

To read the Register:

probe `out`

Result:

`out` emits the Register's state





### Register / write logic

To set Register  = $v$

```
set in = v
set load = 1
```

Result:

- The register's state becomes $v$
- From the next cycle onward,`out` emits v







### Register chip in action





### RAM unit

![image-20210103114030592](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210103JrX1vp.png)





#### RAM / Read Logic

set address = $i$

out emits the state of Register $i$



#### RAM / Write Logic

To set `Register` $$i$$ to $$v$$:

set address = $I$ 

set in = $$v$$

set load = 1



Result:

- The state of `Register` $$i$$ becomes $v$
- From the next cycle onward, out emits $v$





#### In Action

![image-20210103115105857](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210103WGKALr.png)





#### A family of 16-bit RAM chips

