《Practical Vim》（《Vim实用技巧》）笔记，参考了[gitig/Practical-Vim-Notes](https://github.com/gitig/Practical-Vim-Notes) 和`中文版 Practical Vim`，加入了一些我的理解和例子, 教程的[写作方式](part0/tip1.markdown)

## 第1章 Vim 解决问题的方式
技巧 1. [认识`.`命令](part0/tip1.md):  `.`,`x`,`u`,`dd`,`>G`,`h`,`j`,`k`,`l` <br>

技巧 2. [不要自我重复](part0/tip2.md): `$`,`I`,`i`,`a`,`A` <br>

技巧 3. [以退为进](part0/tip3.md): `f{char}`,`;`,`,`,`s` <br>

技巧 4. [执行、重复、回退](part0/tip4.md): `.`,`u` <br>

技巧 5. [查找并手动替换](part0/tip5.md): `:%s/content/copy/g`,`*`,`#` <br>

技巧 6. [结识`.`范式](part0/tip6.md): `.`  <br>

# 第一部分 模式

> 在不同的模式上按键,产生的效果可能不同

## 第2章 普通模式

> 1. 普通模式在执行时可以指定执行次数
> 2. 指定执行次数可以减少按键次数,但是有的时候多按几次更好: 计算按键次数可能费脑子, 不如直接next,next一直到目的地
> 3. 普通模式:操作符+动作命令

技巧 7. [停顿时请移开画笔](part1_pattern/chapter2_normal_pattern/tip7.md)  <br>

技巧 8. [把撤销的单元切成块](part1_pattern/chapter2_normal_pattern/tip8.md): `<Esc>o` <br>

技巧 9. [尽量构造可重复的修改](part1_pattern/chapter2_normal_pattern/tip9.md): [VimGolf](http://vimgolf.com), `daw` vs `dbw` vs `dbx`  <br>

技巧 10. [用次数做简单的算术运算](part1_pattern/chapter2_normal_pattern/tip10.md): `<C-a>`,`<C-x>`,`yyp`,`cw` <br>

技巧 11. [能够重复,就别用次数](part1_pattern/chapter2_normal_pattern/tip12.md): `d3w` vs `3dw` vs `dw..`   <br>

技巧 12. [操作+操作符 双剑合璧](part1_pattern/chapter2_normal_pattern/tip12.md): `gu`,`gU`,`g~`,`=`,`<`,`>` <br>


## 第3章 插入模式

> 1. 大多数操作都在非插入模式中实现(复制\删除\剪切\黏贴)
> 2. 不离开插入模式就可以黏贴寄存器中的文本
> 3. 如何插入键盘上不存在的字符?
> 4. 替换模式是插入模式的特例
> 5. `插入-普通模式`是插入模式的子集


技巧 13. [在插入模式中回退/撤销](part1_pattern/chapter3_insert_mode/tip13.md): `<C-x>`,`<C-w>`,`<C-u>` <br>

技巧 14. [返回普通模式](part1_pattern/chapter3_insert_mode/tip14.md): `<` <br>

技巧 15. [不离开插入模式, 粘贴寄存器中的文本](part1_pattern/chapter3_insert_mode/tip15.md): `yt,`,`<C-r>0`  <br>

技巧 16. [随时随地做运算](part1_pattern/chapter3_insert_mode/tip16.md): `<C-r>=` <br>

技巧 17. [用字符编码插入非常用字符](part1_pattern/chapter3_insert_mode/tip17.md):  `<C-v>{123}`,`<C-v>u{1234}`,`<C-v><CR>`<br>

技巧 18. [用二合字母(digraph)插入非常用字符](part1_pattern/chapter3_insert_mode/tip18.md): `<C-k>35`,`<C-k>?I`,`<C-k><<` <br>

技巧 19. [使用替换模式替换已有文本](part1_pattern/chapter3_insert_mode/tip19.md): `R`,`r` <br>

## 第4章 可视模式

> 1. 可视模式允许在选中的文本区域上操作
> 2. 可视模式分为在字符文本\行文本\块文本上的操作
> 3. `.`命令对于行文本的操作用处较大, 其他可视模式里使用`.`意义不大

技巧 20. [深入理解可视模式](part1_pattern/chapter4_visual_mode/tip20.md): `viw`, `<C-g>`,`c` <br>

技巧 21. [选择高亮区域](part1_pattern/chapter4_visual_mode/tip21.md): `v`,`V`,`<C-v>`,`o`  <br>

技巧 22. [重复执行面向行的可视命令](part1_pattern/chapter4_visual_mode/tip22.md): `Vj>.`  <br>

技巧 23. [尽可能使用操作符命令,而不是可视命令](part1_pattern/chapter4_visual_mode/tip23.md): `vitU`, `gUit`  <br>

技巧 24. [用面向__列块__的可视模式编辑**表格数据**](part1_pattern/chapter4_visual_mode/tip24.md): `<C-v>3jr|`  <br>

技巧 25. [修改列文本](part1_pattern/chapter4_visual_mode/tip25.md): `<C-v>jjec<Esc>` <br>

技巧 26. [在长短不一的高亮块中添加文本](part1_pattern/chapter4_visual_mode/tip26.md): `<C-v>jj$c<Esc>`  <br>

## 第5章 命令行模式

> 1. `ex` 本来是一个行编辑器, 是`vi`的祖先
> 2. 基于行的编辑任务, Ex 命令是最佳工具

技巧 27. [结识Vim的命令行模式](part1_pattern/chapter5_ex_mode/tip27.md): `:`,`<C-w>`  <br>

技巧 28. [在一行或多个连续行上执行命令](part1_pattern/chapter5_ex_mode/tip28.md): `:2,5p`,`:%s/old/new/gc`,`:/<html>/-1,/<\/html>/+1p`  <br>

技巧 29. [使用`:t` `:m` 进行复制和移动行](part1_pattern/chapter5_ex_mode/tip29.md): `:6t.`,`Vjj:m$`  <br>

技巧 30. [在指定范围上执行普通模式命令](part1_pattern/chapter5_ex_mode/tip30.md): `:'<,'>normal .`  <br>

技巧 31. [重复上次的Ex命令](part1_pattern/chapter5_ex_mode/tip31.md):`:@:`, `:bp`,`:bn`  <br>

技巧 32. [自动补全Ex命令](part1_pattern/chapter5_ex_mode/tip32.md):`<Tab>`,`<C-n>`,`<C-p>`  <br>

技巧 33. [把当前单词插入到命令行](part1_pattern/chapter5_ex_mode/tip33.md): `/<C-r><C-w><CR>`, `*:%s//<C-r><C-w>/g`  <br>

技巧 34. [回溯历史命令](part1_pattern/chapter5_ex_mode/tip34.md):`q:`  <br>

技巧 35. [运行Shell命令](part1_pattern/chapter5_ex_mode/tip35.md): `:ls`,`:write! sh`,`:write !sh`,`:2,$!sort -t',' -k2,2`  <br>

# 第二部分 文件

## 第6章 管理多个文件

> 1. 缓冲区列表记录打开的所有文件
> 2. 缓冲区文件分组方法
> 3. 将Ex命令作用在缓冲区每个文件上
> 4. 标签页分割窗口

技巧 36. [用缓冲区列表管理打开的文件](part2_file/chapter6_multi_files/tip36.md):  `:bnext`, `:ls`, `<C-^>`, `:bprev`, `:bfirst`, `:blast`, `:buffer N`, `:buffer {bufname}`, `:bufdo`, `:argdo`, `:bd[elete]`<br>

技巧 37. [用参数列表将缓冲区分组](part2_file/chapter6_multi_files/tip37.md):  `:args {arglist}`<br>

技巧 38. [管理隐藏缓冲区](part2_file/chapter6_multi_files/tip38.md):  `:wirte`, `:edit!`, `qall!`, `:wall`<br>

技巧 39. [将工作区分成窗口](part2_file/chapter6_multi_files/tip39.md):  `<C-w>s`, `<C-w>v`, `:edit`, `:close`, `:only`<br>

技巧 40. [用标签页将窗口分组](part2_file/chapter6_multi_files/tip40.md): `:lcd{path}`, `:tabe[dit] {filename}`, `:tabmove [N]` <br>

## 第7章 打开及保存文件

> 1. 介绍在vim 中打开文件的方式
> 2. 配置`path`选项之后利用`:find` 命令打开文件
> 3. `netrw`插件查看目录树
> 4. 保存文件的时候如果没有**写权限**或是目标路径不存在怎么办？

技巧 41. [用`:edit`命令打开文件](part2_file/chapter7_file_opr/tip41.md): `:edit %<Tab>`, `:edit %:h<Tab>`<br>

技巧 42. [使用`:find`打开文件](part2_file/chapter7_file_opr/tip42.md): `:find`, `:set path+=app/**`<br>

技巧 43. [使用netrw管理文件系统](part2_file/chapter7_file_opr/tip43.md):`:edit .`, `:e.`, `:Explore`, `:E.` <br>

技巧 44. [把文件保存到不存在的目录中](part2_file/chapter7_file_opr/tip44.md): `<C-g>`, `:!mkdir -p %:h`<br>

技巧 45. [以超级用户权限保存文件](part2_file/chapter7_file_opr/tip45.md): `:w !sudo tee % > /dev/null` <br>


# 第三部分 更快的移动和跳转

> 学习vim如何在文件内、文件间快速跳转

## 第8章 用动作命令在文档中快速跳转

> 1. 使用动作（motion）命令在文档中跳转
> 2. 上下左右移动、一次移动一个单词、通过查找命令快速移动
> 3. 操作符待决模式
> 4. 查看vim文档`:h motion`

技巧 46. [让手指保持在 `本位行（Home Row）`上](part3_fast_move/chapter8_doc_jump/tip46.md):  `h,j,k,l`<br>

技巧 47. [区分实际行和屏幕行](part3_fast_move/chapter8_doc_jump/tip47.md):`gj`, `gk`, `g0`, `g$`, `g^`  <br>

技巧 48. [基于单词移动](part3_fast_move/chapter8_doc_jump/tip48.md):`w`, `b`, `e`, `ge`, `ea`, `gea`, `W`, `cW` <br>

技巧 49. [对字符串进行查找](part3_fast_move/chapter8_doc_jump/tip49.md):`f{char}`, `;`, `,`, `F{char}`, `t{char}`, `T{char}`, `dt.`  <br>

技巧 50. [通过查找进行移动](part3_fast_move/chapter8_doc_jump/tip50.md):`/{char}`, `n`, `N`   <br>

技巧 51. [用精确的文本对象选择选取](part3_fast_move/chapter8_doc_jump/tip51.md):`vi}`, `a"`, `i"`, `at`, `it`  <br>

技巧 52. [删除周边，修改内部](part3_fast_move/chapter8_doc_jump/tip52.md):`iw`, `iW`, `is`, `ip`, `aw`, `aW`, `as`, `ap`  <br>

技巧 53. [设置位置标记，以便快速跳回](part3_fast_move/chapter8_doc_jump/tip53.md):`m{a-zA-Z}`, `'{mark}`  <br>

技巧 54. [在匹配括号间跳转](part3_fast_move/chapter8_doc_jump/tip54.md):`%`, `S"`  <br>

## 第9章 在文件间跳转


技巧 55. [遍历跳转列表](part3_fast_move/chapter9_file_jump/tip55.md): `<C-o>`, `<C-i>` <br>

技巧 56. [遍历改变列表](part3_fast_move/chapter9_file_jump/tip56.md):  `:changes`, **`.**, **`^**, `gi` <br>

技巧 57. [跳转到光标下的文件](part3_fast_move/chapter9_file_jump/tip57.md): `gf`, `:set path?` <br>

技巧 58. [用全局位置标记在文件间快速跳转](part3_fast_move/chapter9_file_jump/tip58.md): `:vimgrep`, `` `{char}`` <br>

# 第四部分 寄存器

> 1. 寄存器是保存文本的容器
> 2. 寄存器可以实现复制、粘贴、剪切文本; 可以记录一系列按键操作，制作宏命令

## 第10章 复制和粘贴

> 1. vim提供几十个寄存器保存文本，比系统单一的剪切板多很多
> 2. vim的粘贴可以面向行和面向字符
> 3. 可视模式下的粘贴、系统剪切板的使用

技巧 59. [用无名寄存器实现删除、复制和粘帖操作](part4_register/chapter10_copy_paste/tip59.md):  `x`, `p`, `xp`, `dd`, `ddp`, `yyp`, `P`, `diw`  <br>

技巧 60. [深入理解vim寄存器](part4_register/chapter10_copy_paste/tip60.md): `"{register}`, `"ayiw`, `"bdd`, `"ap`, `"bp`, `""p`, `"0P`, `:reg "0`, `"_d{motion}`, `"+`, `"+p <C-r>+`  <br>

技巧 61. [用寄存器中的内容替换高亮选取的文本](part4_register/chapter10_copy_paste/tip61.md):   `m{char}`, `` `{char}``<br>

技巧 62. [把寄存器中的内容粘贴出来](part4_register/chapter10_copy_paste/tip62.md): `<C-r>{register}`, `p`, `P`, `gp`, `gP`  <br>

技巧 63. [与系统粘贴板进行交互](part4_register/chapter10_copy_paste/tip63.md): `:set pastetoggle=<f5>`, `"+p`   <br>

## 第11章 宏

> 1. 宏是`.`指令的加强版
> 2. 宏适合对一系列相似的行、段落、文件上操作
> 3. 宏的执行分2种方式：串行方式回放 和 并行方式多次运行

技巧 64. [宏的读取和执行](part4_register/chapter11_macro/tip64.md): `q`, `q{register}`, `:reg a`, `@{register}`, `@@`    <br>

技巧 65. [规范光标位置、直达目标以及终止宏](part4_register/chapter11_macro/tip65.md):   `{number}@a` <br>

技巧 66. [加次数回放宏](part4_register/chapter11_macro/tip66.md):   `qq;.q`   <br>

技巧 67. [在连续的文本行上重复修改](part4_register/chapter11_macro/tip67.md):   `0`, `:normal @a`  <br>

技巧 68. [给宏追加命令](part4_register/chapter11_macro/tip68.md):   `qa`, `qA` <br>

技巧 69. [在一组文件中执行宏](part4_register/chapter11_macro/tip69.md):    `gg/class<CR>`, `:argdo`, `:edit!`, `:argdo normal @a`, `:argdo write`, `:wall`, `:wnext`   <br>

技巧 70. [用迭代求值的方式给列表编号](part4_register/chapter11_macro/tip70.md):   `:let i=0`, `:echo i`, `<C-r>=i<CR>`  <br>

技巧 71. [编辑宏的内容](part4_register/chapter11_macro/tip71.md):    `~`, `vU`, `:put a`  <br>

# 第五部分 模式

> 1. pattern使得构造正则表达式和原义查找文本变得容易
> 2. substitute和global是2个强大的Ex命令

## 第12章 按模式匹配和按原义匹配

> 1. 查找时替换的前提，如何在查找时使用正则表达式？
> 2. `very magic`、`very nomagic`模式、原义开关都是什么，什么用？
> 3. 零宽度定界符有哪些？各自作用是？

技巧 72. [调整查找模式的大小写敏感性](part5_pattern/chapter12_match/tip72.md): `\c`, `\C`

技巧 73. [使用`\v`模式进行正则表达式查找](part5_pattern/chapter12_match/tip73.md): `\v`

技巧 74. [完全匹配字符串时，使用`\V` 查找](part5_pattern/chapter12_match/tip74.md):  `\V`

技巧 75. [使用圆括号`()`获取子匹配](part5_pattern/chapter12_match/tip75.md):  `()`

技巧 76. [使用`<`,`>`界定单词边界](part5_pattern/chapter12_match/tip76.md): `<`, `>`

技巧 77. [界定匹配的边界（使用`\zs`, `\ze`）](part5_pattern/chapter12_match/tip77.md): `\zs`, `\ze`

技巧 78. [转移问题字符](part5_pattern/chapter12_match/tip78.md): `/\?`需要转义

## 第13章 查找 

> 1. 查找模式可以自动补全匹配、减少按键次数、统计匹配数量
> 2. 构造正确的正则表达式一般需要调试多次，我们可以迭代的构造模式，减少调试代价
> 3. 可以定制命令，查找高亮选区的文本
> 4. 定制自己的`*`，在可视模式下也可快速查找选中的文本

技巧 79. [查找命令入门](part5_pattern/chapter13_search/tip79.md): `/`, `?`, `n`, `N`

技巧 80. [高亮查找匹配](part5_pattern/chapter13_search/tip80.md): `hlsearch`, `noh`, `<C-l>`

技巧 81. [在执行查找前预览第一处匹配](part5_pattern/chapter13_search/tip81.md): `incsearch`, `<C-r><C-w>`

技巧 82. [统计当前模式的匹配个数](part5_pattern/chapter13_search/tip82.md): `:%s///gn`

技巧 83. [将光标偏移到查找匹配的结尾](part5_pattern/chapter13_search/tip83.md): `/xxxx/e`

技巧 84. [对完整的查找匹配进行操作](part5_pattern/chapter13_search/tip84.md): `/\vX(ht)?ml\C`,`gUfl`

技巧 85. [利用查找历史， 迭代完成复杂的模式](part5_pattern/chapter13_search/tip85.md): `:%s/\v'(([^']|'\w)+)'/“\1”/g`

技巧 86. [查找当前高亮选区中的文本](part5_pattern/chapter13_search/tip86.md): `y/<C-R>"`

## 第14章 替换

> 1. 替换和查找是最常用的vim命令
> 2. 替换命令中的查找域可以为空
> 3. 替换命令支持跨文件操作
> 4. 替换命令中的替换域支持脚本表达式，实现复杂操作

技巧 87. [结识 substitute 命令](part5_pattern/chapter14_substitute/tip87.md): `：[range]s/{pattern}/{string}/[flags]`

技巧 88. [在文件范围内查找并替换每一处匹配](part5_pattern/chapter14_substitute/tip88.md): `:%s/going/rolling/g`

技巧 89. [手动控制每一次替换操作](part5_pattern/chapter14_substitute/tip89.md): `:%s/content/copy/gc`

技巧 90. [重用上次的查找模式](part5_pattern/chapter14_substitute/tip90.md): `:%s//“\1”/g`, `:%s/\n/,/g`, `:%s/<C-r>//“\1”/g` 

技巧 91. [用寄存器的内容替换](part5_pattern/chapter14_substitute/tip91.md): `:%s//<C-r>0/g`

技巧 92. [重复上一次 substitute 命令](part5_pattern/chapter14_substitute/tip92.md): `:%s//~/&`, `g&`, `:%s/Name/Number/g`, `:%&&`

技巧 93. [使用子匹配重排CSV文件的字段](part5_pattern/chapter14_substitute/tip93.md): `/\v^([^,]*),([^,]*),([^,]*)$`、`:%s//\3,\2,\1`

技巧 94. [在替换过程中执行算术运算 ](part5_pattern/chapter14_substitute/tip94.md): `/\v\<\/?h\zs\d`, `:%s//\=submatch(0)-1/g`

技巧 95. [交换两个或更多的单词](part5_pattern/chapter14_substitute/tip95.md): `:%s//\={"dog":"man","man":"dog"}[submatch(1)]/g`

技巧 96. [在多个文件中执行查找与替换](part5_pattern/chapter14_substitute/tip96.md): `:argdo %s//Practical/g`, `:vimgrep /<C-r>// **/*.txt`

## 第15章 global 命令

> 1. global 命令融合了Ex命令与Vim模式匹配的能力
> 2. 可以在指定模式的所有匹配行上运行Ex命令
> 3. global 命令是除了点范式和宏以外，最强大的Vim工具

技巧 97. [结识 global 命令](part5_pattern/chapter15_global_cmd/tip97.md): `:[range] global[!] /{pattern}/ [cmd]`

技巧 98. [删除所有包含模式的文本行](part5_pattern/chapter15_global_cmd/tip97.md): `/\v\<\/?\w+>`,`:g//d`,`:v/href/d`,`:g/re/p`

技巧 99. [将 TODO 项收集至寄存器](part5_pattern/chapter15_global_cmd/tip97.md): `:global`,`:yank`

技巧 100. [将 CSS 文件中所有规则的属性按照字母排序](part5_pattern/chapter15_global_cmd/tip100.md): `:g/{/ .+1,/}/-1 sort`


# 第六部分 工具

> 1. vim内可以方便调用make、grep等外部程序
> 2. vim提供拼写检查和自动补全等命令

## 第16章 通过 ctags 建立索引，并用其浏览源代码

> 1. ctags使我们可以快速跳到函数和类的定义处，实现浏览整个代码库
> 2. ctags的结果也可以用于自动补全

技巧 101. [结识ctags](part6_tools/chapter16_ctags/tip101.md): `ctags *`

技巧 102. [配置 Vim 使用 ctags](part6_tools/chapter16_ctags/tip102.md): `:set tags?`,`:!ctags -R`

技巧 103. [使用 Vim 的标签跳转命令，浏览关键字的定义](part6_tools/chapter16_ctags/tip103.md): `<C-t>`,`<C-]>`,`g<C-]>`,`:tag {keyword}`,`:tjump {keyword}`

## 第17章 编译代码，并通过 Quickfix 列表浏览错误信息

> 1. quickfix列表会维护乙组文件名、行号、列号（可选）与消息组成的注释定位信息
> 2. 可以使用`:make`命令编译，并将错误信息进行解析，在quickfix列表中提供浏览

技巧 104. [不用离开 Vim 也能编译代码](part6_tools/chapter17_compile/tip104.md): `make`, `:cnext`

技巧 105. [浏览 Quickfix 列表](part6_tools/chapter17_compile/tip105.md): `:cprev`,`:cnext`,`:cfirst`,`:clast`,`:cnfile`,`:cpfile`,`:cc N`, `:copen`

技巧 106. [回溯以前的 Quickfix 列表](part6_tools/chapter17_compile/tip106.md): `:colder`,`:cnewer`, `:5colder`

技巧 107. [定制外部编译器](part6_tools/chapter17_compile/tip107.md): `:setglobal errorformat?`


## 第18章  通过 grep、vimgrep 以及其他工具对整个工程进行查找

> 1. `:grep`可以在不离开vim下调用外部程序
> 2. `:gep`可以调用grep，也可以调用ack
> 3. `:vimgrep`允许在多个文件中指定查找模式

技巧 108. [不必离开 Vim 也能调用 grep](part6_tools/chapter18_grep_search/tip108.md): `:grep Waldo *`

技巧 109. [定制grep程序](part6_tools/chapter18_grep_search/tip109.md): `grepprg`,`grepformat`

技巧 110. [使用 Vim 内部的 Grep](part6_tools/chapter18_grep_search/tip110.md): `:vimgrep`,`vim /<C-r>// **`
 

## 第19章 自动补全

> 1. vim可以从限定的来源（缓冲区文件、头文件、标签文件）来进行自动补全
> 2. 介绍如何从补全列表中获取正确的单词，以及如何获取相关度最高的补全建议

技巧 111. [结识 Vim 的关键字自动补全](part6_tools/chapter19_auto_complete/tip111.md): `<C-p>`,`<C-n>`,`<C-x>`

技巧 112. [与自动补全的弹出式菜单进行交互](part6_tools/chapter19_auto_complete/tip112.md): `<C-n>`等价于`<Down>`;`<C-p>`等价于`<Up>`

技巧 113. [掌握关键字的来龙去脉](part6_tools/chapter19_auto_complete/tip113.md): `<C-x><C-n>`,`<C-x><C-i>`,`<C-x><C-]>`

技巧 114. [使用字典中的单词进行自动补全](part6_tools/chapter19_auto_complete/tip114.md): `<C-x><C-k>`,`:set spell`

技巧 115. [自动补全整行文本](part6_tools/chapter19_auto_complete/tip115.md) 

技巧 116. [自动补全文件名](part6_tools/chapter19_auto_complete/tip116.md): `<C-x><C-f>`

技巧 117. [根据上下文自动补全](part6_tools/chapter19_auto_complete/tip117.md): `<C-x><C-o>`

## 第20章 利用 Vim 的拼写检查器，查找并更正拼写错误

> 1. vim的拼写检查可以针对不同语言/地区使用不同的规则
> 2. 插入模式下也可以使用拼写检查
> 3. 可以对拼写检查的单词表进行自定义（添加/删除）

技巧 118. [对你的工作进行拼写检查](part6_tools/chapter20_spell_check/tip118.md): `[s`,`]s`,`2z=`

技巧 119. [使用其他拼写字典](part6_tools/chapter20_spell_check/tip119.md): `:set spelllang=en_us`

技巧 120. [将单词添加到拼写文件中](part6_tools/chapter20_spell_check/tip120.md): `zg`,`zw`

技巧 121. [在插入模式下更正拼写错误](part6_tools/chapter20_spell_check/tip121.md): `<C-x>s`
