## VM Implementation on the Hack Platform

### VM translator 

![image-20210107130335030](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107Ptjuxz.png)

Each VM command is translated into several assembly commands



In order to write a VM translator, we must be familiar with:

- The source language
- The target language
- The VM mapping on the target platform



### Source: VM language

![image-20210107130551769](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107AVoORM.png)



### Target: Symbolic Hack code

![image-20210107130625740](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107KzgwjL.png)



### Standard VM mapping on the Hack platform

VM mapping decisions:

- How to map the VM's data structure using the host hardware platform
- How to express the VM's commands using the host machine language



Standard mapping :

- Specifies how to do the mapping in an agreed-upon way
- Benefit:
  - Compatibility with other software systems
  - Standard testing 

![image-20210107130933878](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107v7BlDS.png)



In order to realize this mapping , the VM translator should use some special variables / symbols:



![image-20210107131227357](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210107gVy77n.png)