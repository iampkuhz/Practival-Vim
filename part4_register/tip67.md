#Tip67: Repeat a Change on Contiguous Lines  
We want to make a change: 
![tip67_1](images/tip67_1.png)  
![tip67_2](images/tip67_2.png)  
  
**Record One Unit of Work**  
  
![tip67_3](images/tip67_3.png)  
  
##0  
>normalizes our cursor position by placing it at the start of the line. This means that our next motion always starts from the same place, making it more repeatable.  
  
Note: `f.` is more repeatability than `l`  
  
**Execute Macro in Series**  
![tip67_4](images/tip67_4.png)  
  
![tip67_5](images/tip67_5.png)  
  
When the `f.` command is executed, it finds no . characters and the macro aborts.  
  
![tip67_6](images/tip67_6.png)  
  
**Execute Macro in Parallel**  
![tip67_7](images/tip67_7.png)  
  
##:normal @a  
>tells Vim to execute the macro once for each line in the selection.  
  
**Deciding: Series or Parallel**  
Executing a macro on multiple items in parallel is more robust.  
  
#[Tip66](tip66.md) [Tip68](tip68.md)
