## Counters

#### Where counter come to play





### Counter abstraction

![image-20210103120708794](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210103yoo1o6.png)

```hdl
/**
 *if(reset[t]==1) out[t+1] = 0
 *else if (load[t]==1) out[t+1] = in[t]
 *		else if (inc[t]==1) out[t+1] = out[t] + 1
 *				else out[t+1] = out[t]
 */
```

