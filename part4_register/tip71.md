#Tip71: Edit the Contents of a Macro  
**The Problem: Nonstandard Formatting**  
![tip71_1](images/tip71_1.png)  
  
##~  
>toggles the case of the letter under the cursor.  
  
##vU  
>uppercase the letter under the cursor.  
  
**Paste the Macro into a Document**  
##:put a  
>paste the macro into the document(below the current line).  
>`"ap` paste the contents of a register after the cursor position on the current line.  
  
**Edit the Text**  
![tip71_2](images/tip71_2.png)  
  
**Yank the Macro from the Document Back into a Register**  
##"add  
>the dd command performs a line-wise deletion, the register contains a trailing ^J character.  
>this character represents a newline.  
  
As a precaution, using a character-wise yank:  
![tip71_3](images/tip71_3.png)  
  
##"ay$  
>yank every character on that line except for the carriage return.  
  
**Discussion**  
##:let @a=substitute(@a, '\~', 'vU', 'g')  
>perform the same edit as before.  
  
#[Tip70](tip70.md) [Tip72](tip72.md)
