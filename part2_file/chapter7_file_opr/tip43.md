# 技巧43： 使用netrw管理文件系统

> `netrw`全称是`across NETwork Read and Write files`

vimrc 需要配置下面的内容
> set nocompatible <br>
> filetype plugin on


1. shell 命令行输入命令`vim .`，显示如下. 按`jk`移动光标，按回车键选中文件
![tip43_1](../../images/tip43_1.png)  

2. `:edit .`打开文件管理器
3. `:Explore` 打开netrw的文件管理器
> `:E.` 等价`:Explore`，（但貌似不是通用的，我的不可以）

`工程目录树(project drawer)`: 一般的文本编辑软件的布局结构，左侧边是目录管理器的结构

## 与分割窗口协同工作

> `:Explore` 默认在活动窗口打开新文件

`<C-^>`打开上一次的文件（**如果上一次打开的是目录，则会报错**）

下图说明：**用工程目录树打开的新文件在原来的窗口显示**

![tip43_0](../../images/tip43_0.png)  
<br>  

|上一篇|下一篇|
|:---|---:|
|[技巧42 使用`:find`打开文件](tip42.md)|[技巧44 把文件保存到不存在的目录中](tip44.md)|
