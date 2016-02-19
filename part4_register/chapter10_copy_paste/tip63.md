# 技巧63: 与系统粘贴板进行交互
> 如果vim启用`autoindent`选项，则在插入命令下插入系统粘贴板的时候可能排版会混乱

### 例子：从系统粘贴板复制一段代码

1. 待插入代码如下：<br>
![tip63_0](../../images/tip63_0.png)
2. 我们在别的程序中打开这个文件，并复制到系统粘贴板
3. 在vim中进入插入模式，然后使用系统的粘贴命令（`Ctrl+V`）插入这段代码，效果如下：<br>
![tip63_1](../../images/tip63_1.png)

这是因为`autoindent`选项启用后每次插入一个新行（输入了一个`<CR>`），就会增加一层缩进，所以排版出错

#### 设置`paste`选项可以避免系统剪切板的粘贴操作出现意外，但是粘贴完后必须`尽快关闭paste选项`，否则插入模式下创建的自定义映射都会失效

为了解决上面切换的代价，2种方式：

1. 设置`set pastetoggle=<F5>`,按`<F5>`来启动/关闭`paste`选项
2. **推荐：** 使用家好寄存器进行粘贴`，"+p`将寄存器的内容粘贴到光标之后，不论`autoindent`是否启用，都能保证排版不会出错




#Tip63: Interact with the System Clipboard  
Besides Vim's built-in put commands, we can sometimes use the system paste command. However, using this can occasionally produce unexpected results when running Vim inside a terminal. We can avoid these issues by enabling the 'paste' option before using the system paste command.  

When we use the system paste command in Insert mode, Vim acts as though each character has been typed by hand. When the 'autoindent' option is enabled, Vim preserves the same level of indentation each time we create a new line. The leading whitespace at the start of each line in the clipboard is added on top of the automatic indent, and the result is that each line wanders further and further to the right.  

GVim is able to discern when text is pasted from the clipboard and adjust its behavior accordingly, but when Vim runs inside a terminal this information is not available. The 'paste' option allows us to manually warn Vim that we're about to use the system paste command. When the 'paste' option is enabled, Vim turns off all Insert mode mappings and abbreviations and resets a host of options, including 'autoindent'. That allows us to safely paste from the system clipboard with no surprises.  

When we're finished using the system paste command, we should disable the 'paste' option again. That means switching back to Normal mode and then running the Ex command `:set paste!`. Don't you think it would be handly if there were a way of toggling this option without leaving Insert mode?  

##:set pastetoggle=&lt;f5&gt;  
>sets up the `<f5>` to toggle the paste option on and off.  

**Avoid Toggling 'paste' by Putting from the Plus Register**  
If you're running a version of Vim with system clipboard integration, then you can avoid fiddling with the 'paste' option entirely. The Normal mode `"+p` command pastes the contents of the plus register, which mirrors the system clipboard. This command preserves the indentation of the text in the clipboard so you can expect no surprises, regardless of how the 'paste' and 'autoindent' options are set.  

#[Tip62](tip62.md) [Tip64](tip64.md)
