#Tip66: Play Back with a Count  
The dot Formula can be an efficient editing strategy for a small number of repeats, but it can't be executed with a count. Overcome this limitation by recording a cheap one-off macro and playing it back with a count.  
  
##qq;.q  
>`qq` tells Vim to record the following keystrokes and save them to the q register.  
>`;.` our commands.  
>`q` finish recording the macro.  
  
The `;` command repeats the `f+` search. When our cursor is positioned after the last + character on the line, the `;` motion fails and the macro aborts.  
  
![tip66](images/tip66.png)  
  
In our case, we want to execute the macro ten times. But if we were to play it back eleven times, the final execution would abort.  
In other words, we can complete the task so long as we invoke the macro with a count of ten or more.  
I often use 22, because I'm lazy and it's easy to type.  
  
#[Tip65](tip65.md) [Tip67](tip67.md)
