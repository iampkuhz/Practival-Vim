#Tip65: Normalize, Strike, Abort  
Executing a macro can sometimes produce unexpected results, but we can achieve better consistency if we follow a handful of best practices.  
  
When we execute a macro, Vim blindly repeats the sequence of canned keystrokes.  
  
The golden rule is this: when recording a macro, ensure that every command is repeatable.  
  
**Normalize the Cursor Position**  
Before you do anything, make sure your cursor is positioned so that the next command does what you expect, where you expect it.  
  
**Strike Your Target with a Repeatable Motion**  
Word-wise motions, such as `w`, `b`, `e` and `ge` tend to be more flexible than character-wise `h` and `l` motions.  
Don't forget: when recording a macro, using the mouse is **verboten**.  
  
**Abort When a Motion Fails**  
If a motion fails while a macro is executing, then Vim aborts the rest of the macro.  
  
##number@a  
>rather than executing `@a` ten times. We could prefix it with a count: `10@a`.  
  
#[Tip64](tip64.md) [Tip66](tip66.md)
