# 技巧95: 交换两个或更多的单词
> 使用表达式寄存器+Vim脚本中的字典数据结构，对多个单词进行互换

### 例子: 交换`dog`和`man`
> ![](../../images/tip94.png)

1. 错误解决方案：执行2条指令`:%s/dog/man/g`、`:%s/man/dog/g`
    1. 第一条指令执行完后，会有2个`man`，再执行第二条会错误
2. 使用字典的解决方案：
    0. 实验vim的字典：`:let swapper={"dog":"man","man":"dog"}`
        1. 执行完后可以查询字典：`:echo swapper["dog"]`，`:echo swapper["man"]`
    1. 解决方案part1：`/\v(<man>|<dog>)`
    2. 解决方案part2：`:%s//\={"dog":"man","man":"dog"}[submatch(1)]/g`

|上一篇|下一篇|
|:---|---:|
|[技巧94: 在替换过程中执行算术运算 ](tip94.md)|[技巧96: 在多个文件中执行查找与替换](tip96.md)|
