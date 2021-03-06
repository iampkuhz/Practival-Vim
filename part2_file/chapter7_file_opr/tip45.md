# 技巧45： 以超级用户权限保存文件

> 我们想要修改一个文件，但是直接`vim file` 打开了一个只读文件忘记`sudo vim file`, 当我们第一次修改这个文件时，会提示`warning，XXXXX`，但结果我们连这个warning也没有看到，一直修改了好长时间，结果最后`:w`想保存的时候发现保存不了,`:w!`也不行，这时候该怎么办？

1. 对于只能读取，不能修改的文件，按`<C-g>`会提示`[readonly]`
2. 对于上面问题的解决方法：

#### `:write !sudo tee % > /dev/null`
> `%`表示编辑的文件的路径
> tee 用法：
> > 1. `tee {filepath}`，监听标准输入，把标准输入存到`{filepath}`上
> > 2. `tee -a {filepath}`,把标准输入**追加**到`{filepath}`中
> `> /dev/null` 重定向标准输出到垃圾桶（不显示标准输出），因为tee在接收标准输入的时候默认会同时打印出来，这个不必要，只要写到文件里就行
> 实际是启动`sudo tee % > /dev/null` 来写文件，然后使用`:write`来把缓冲区作为命令的标准输入


<br>  

|上一篇|下一篇|
|:---|---:|
|[技巧44 把文件保存到不存在的目录中](tip44.md)|[技巧46 用动作命令在文档中移动](../../part3_fast_move/chapter8_doc_jump/tip46.md)|
