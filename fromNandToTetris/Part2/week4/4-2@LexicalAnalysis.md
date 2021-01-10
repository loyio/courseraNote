## Lexical Analysis



### Tokenizing (first approximation)

![image-20210110092930892](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210110xj1j9s.png)

A token is a string of characters that has a meaning

A programming language specification must document (among over whitings ) it's allowable tokens



### Jack tokens

![image-20210110093144812](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210110rVbQhS.png)



Tokenizer:

- Handles the compilers's input
- Allows advancing the input
- Supplies the current token's value and token (complete API, later)



![image-20210110093341273](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210110o736sj.png)



TokenizerTest (pseudo code)

![image-20210110093548027](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210110vLXf8p.png)



