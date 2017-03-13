# 技巧78： 转移问题字符
> 1. `\V`(very nomagic)模式关闭了`.,+*`等字符的特殊含义，但是还有一些字符仍然需要转移
> 2. `/`,`\`,`?` 这几个字符永远都需要转移

1. `/`,`?`字符作为激活查找模式的保留字，如果查找这个字符，则永远都需要转移
2. 转义字符`\`本身也需要转义

### 例子：如何匹配一些奇怪的URL

#### 匹配: `http://vimdoc.net/search?q=/\\`

1. `/\Vhttp://vimdoc.net/search?q=/\\`只能匹配到`http:`
2. `/\Vhttp:\/\/vimdoc.net\/search?q=\/\\`只能匹配到`http://vimdoc.net/search?q=/\`
3. `/\Vhttp:\/\/vimdoc.net\/search?q=\/\\\\` 是正确答案

#### 逆向匹配(`?`): `http://vimdoc.net/search?q=/\\`
1. `?http://vimdoc.net/search?q=/\\` 只能匹配 `http://vimdoc.net/search`
2. `?http://vimdoc.net/search\?q=/\\` 只能匹配 `http://vimdoc.net/search?q=/\`
3. `?http://vimdoc.net/search\?q=/\\\\` 是正确答案


|上一篇|下一篇|
|:---|---:|
|[技巧77： 界定匹配的边界（使用`\zs`, `\ze`）](tip77.md)|[技巧79: 查找命令简介](../chapter13_search/tip79.md)|
