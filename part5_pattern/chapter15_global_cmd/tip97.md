# 技巧97: 结识 global 命令
> global命令允许在指定模式上的所有匹配运行Ex命令

`:[range] global[!] /{pattern}/ [cmd]`

1. `:global`命令的作用范围默认是整个文件（`%`）
    1. 其他Ex命令(删除、替换命令)缺省的作用范围是当前行
2. `{pattern}`域与查找历史相关联，留空则使用之前的查找模式
3. `[cmd]`可以是除`:global`命令之外的任何Ex命令
4. 将`:global`替换为`:global!`或者`:vglobal`(v表示invert)，表示在没有匹配`{pattern}`的行上执行`[cmd]`操作

|上一篇|下一篇|
|:---|---:|
|[技巧96: 在多个文件中执行查找与替换](../chapter14_substitute/tip96.md)|[技巧98: 删除所有包含模式的文本行](tip98.md)|
