#Tip70: Evaluate an Iterator to Number Items in a List  
Being able to insert a value that changes for each execution of a macro can be useful. In this tip, we'll learn a technique for incrementing a number as we record a macro so that we can insert the numbers 1 to 5 on consecutive lines.  
  
![tip70_1](images/tip70_1.png)  
  
**Rudimentary Vim Script**  
##:let i=0  
>create a variable called i and assign it a value of 0.  
  
##:echo i  
>allows us to inspect the current value assigned to a variable.  
  
##&lt;C-r&gt;=i&lt;CR&gt;  
>insert the value stored in variable.  
  
**Record the Macro**  
![tip70_2](images/tip70_2.png)  
  
**Execute the Macro**  
![tip70_3](images/tip70_3.png)  
  
##:normal @a  
>tells Vim to execute the macro on each of the selected lines.  
>the value of i gets incremented each time the macro executes.  
  
#[Tip69](tip69.md) [Tip71](tip71.md)
