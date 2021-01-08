## VM Implementation on the Hack Platform

### The big picture: program compilation and translation

![image-20210108113728450](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108GHwvB9.png)





### Booting 

VM programming convention

One file in any VM program is expected to be named Main.vm; one VM function in this file is expected to be named main



VM implementation convention

When the VM implementation start running, or is reset, it starts executing the argument-less OS function Sys.init

Sys.init then call Main.main, and enters an infinite loop



<u>Hardware platform convention</u>

Bootstrap code





### Standard mapping for the VM on the Hack platform

![image-20210108114404697](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/202101081T3rbi.png)





### Special symbols in VM programs

![image-20210108114457051](https://loyioblog.oss-cn-beijing.aliyuncs.com/LoyioBlog/20210108OpNZMk.png)

