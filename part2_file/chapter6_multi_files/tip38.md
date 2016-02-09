# 技巧38： 管理隐藏缓冲区

#Tip38: Manage Hidden Files  

When a buffer has been modified, Vim gives it special treatment to ensure that we don't accidentally quit the editor without saving our changes, Find out how to hide a modified buffer and how to handle hidden buffers when quiting Vim.  

![tip38_1](../../images/tip38_1.png)  

![tip38_2](../../images/tip38_2.png)  


**Handle Hidden Buffers on Quit**  

When you quit Vim and have unsaved changes in one of buffers. Vim loads the first hidden buffer with modifications into the current window so that we can decide what to do with it.  

##:write  
> to save the buffer to a file.  

##:edit!  
> to discard the changes(reread the file from disk, overwriting the contents of the buffer)  

Vim activates the next unsaved buffer each time we enter the `:quit` command  

##:qall!  
> quit Vim without reviewing our unsaved changes.  

##:wall  
> write all modified buffers without reviewing them one by one.  

![tip38_3](../../images/tip38_3.png)  


**Enable the `hidden` Setting Before Running `:argdo` or `:bufdo`**  

Be default, Vim prevents us from abandoning a modified buffer.  

![tip38_4](../../images/tip38_4.png)  

#[Tip37](tip37.md) [Tip39](tip39.md)
