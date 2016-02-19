#Tip68: Append Commands to a Macro  
Sometimes we miss a vital step when we record a macro. There's no need to re-record the whole thing from scratch. Instead, we can tack extra commands onto the **end** of an existing macro.  
![tip68_1](images/tip68_1.png)  
  
We realize that we should have finished by pressing `j` to advance to the next line.  
  
Before we fix it, let's inspect the contents of register a:  
![tip68_2](images/tip68_2.png)  
  
##qa  
>Vim will record our keystrokes, saving them into register a by overwriting the existing contents of that register.  
  
##qA  
>Vim will record our keystrokes, **appending** them to the existing contents of register a.  
  
![tip68_3](images/tip68_3.png)  
  
**Discussion**  
We can use this tech only to tack commands on at the **end** of a macro. If you want to add something at the beginning or somewhere in the middle of a macro, this technique would be no use to you!  
  
#[Tip67](tip67.md) [Tip69](tip69.md)
