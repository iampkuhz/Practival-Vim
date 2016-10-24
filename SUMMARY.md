# Summary

* [Introduction](README.md)

  *《Practical Vim》（《Vim实用技巧》）笔记，参考了[gitig/Practical-Vim-Notes](https://github.com/gitig/Practical-Vim-Notes) 和`中文版 Practical Vim`，加入了一些我的理解和例子, 教程的[写作方式](tip1.markdown)

* [第〇部分 基本操作说明](第〇部分-基本操作说明.md)
  * [第1章 Vim 解决问题的方式](第1章-vim-解决问题的方式.md)
    * [认识.命令](part0/tip1.md)
    * [不要自我重复](part0/tip2.md)
    * [以退为进](part0/tip3.md)
    * [执行、重复、回退](part0/tip4.md)
    * [查找并手动替换](part0/tip5.md)
    * [结识.范式](part0/tip6.md)



* 第一部分 模式

  * 第2章 普通模式
```
> 1. 普通模式在执行时可以指定执行次数
> 2. 指定执行次数可以减少按键次数,但是有的时候多按几次更好: 计算按键次数可能费脑子, 不如直接next,next一直到目的地
> 3. 普通模式:操作符+动作命令
```
    * [停顿时请移开画笔](part1_pattern/chapter2_normal_pattern/tip7.md)
    * [把撤销的单元切成块](part1_pattern/chapter2_normal_pattern/tip8.md)
    * [尽量构造可重复的修改](part1_pattern/chapter2_normal_pattern/tip9.md)
    * [用次数做简单的算术运算](part1_pattern/chapter2_normal_pattern/tip10.md)
    * [能够重复,就别用次数](part1_pattern/chapter2_normal_pattern/tip12.md)
    * [操作+操作符 双剑合璧](part1_pattern/chapter2_normal_pattern/tip12.md)

  * 第3章 插入模式
```
> 1. 大多数操作都在非插入模式中实现(复制\删除\剪切\黏贴)
> 2. 不离开插入模式就可以黏贴寄存器中的文本
> 3. 如何插入键盘上不存在的字符?
> 4. 替换模式是插入模式的特例
> 5. `插入-普通模式`是插入模式的子集
```
    * 技巧 13. [在插入模式中回退/撤销](part1_pattern/chapter3_insert_mode/tip13.md): `<C-x>`,`<C-w>`,`<C-u>`
    * 技巧 14. [返回普通模式](part1_pattern/chapter3_insert_mode/tip14.md): `<` 
    * 技巧 15. [不离开插入模式, 粘贴寄存器中的文本](part1_pattern/chapter3_insert_mode/tip15.md): `yt,`,`<C-r>0`
    * 技巧 16. [随时随地做运算](part1_pattern/chapter3_insert_mode/tip16.md): `<C-r>=` <br>
    * 技巧 17. [用字符编码插入非常用字符](part1_pattern/chapter3_insert_mode/tip17.md): `<C-v>{123}`,`<C-v>u{1234}`,`<C-v><CR>`<br>
    * 技巧 18. [用二合字母(digraph)插入非常用字符](part1_pattern/chapter3_insert_mode/tip18.md): `<C-k>35`,`<C-k>?I`,`<C-k><<` <br>
    * 技巧 19. [使用替换模式替换已有文本](part1_pattern/chapter3_insert_mode/tip19.md): `R`,`r` <br>

