# 技巧96: 在多个文件中执行查找与替换
> vim 本身没有提供跨文件的替换命令，我们可以通过命令组合间接实现

### 例子：将每个文件中的`Pragmatic Vim`替换为`Pragmatic Practical`

解决步骤：
1. 在一个文件中执行：`/Pragmatic\ze Vim`和`:%s//Practical/g`
2. 将所有待处理文件加入到参数列表：`:args **/*.txt`
3. 执行：`:set hidden` (允许在有未保存的修改时切换缓冲区)
4. 执行：`:argdo %s//Practical/g` 对缓冲区中的每个文件执行替换操作
    1. 如果有的文件并不能找到替换的地方，则会报"找不到模式"的提示，可以使用`:argdo %s//Practical/ge`来忽略提示

另一种解决方法（假设所有待替换的文件都已经在vim的缓冲区列表中了）：
```angular2html
// 当前文件中进行查找
/Pragmatic\ze Vim
// 对缓冲区
:vimgrep /<C-r>// **/*.txt
:Qargs
:argdo %s//Practical/g
:argdo update
```

|上一篇|下一篇|
|:---|---:|
|[技巧95: 交换两个或更多的单词](tip95.md)|[技巧97: 结识 global 命令](../chapter15_global_cmd/tip97.md)|
