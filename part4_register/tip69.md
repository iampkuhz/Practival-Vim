#Tip69: Act Upon a Collection of Files  
So far, we've stuck to tasks that were repeated in the same file, but we can play back a macro across a collection of files. Once again, we'll consider how to execute the macro in parallel and in series.  
  
![tip69_1](images/tip69_1.png)  
  
**Preparation**  
**Build a List of Target Files**  
![tip69_2](images/tip69_2.png)  
  
**Record a Unit of Work**  
![tip69_3](images/tip69_3.png)  
  
![tip69_4](images/tip69_4.png)  
  
##gg/class&lt;CR&gt;  
>`gg` places the cursor at the start of the file.  
>`/class<CR>` jumps forwards to the first occurrence of the word "class".  
  
**Execute the Macro in Parallel**  
##:argdo  
>allow us to execute an Ex command once for **each buffer** in the argument list.  
  
##:edit!  
>revert all of the changes we just made to the first buffer in the argument list.  
  
##:argdo normal @a  
>execute the macro in all of the buffers in the argument list.  
  
**Execute the Macro in Series**  
Our macro performs a single unit of work on a single buffer. If we want to make it act upon multiple buffers, we could append a final step that advances to the next buffer in the list.  
Then we can run `3@a` to execute the macro on each of the remaining files in the buffer list. When we reach the last buffer in the argument list, the `:next` command fails and the macro aborts.  
  
![tip69_5](images/tip69_5.png)  
  
**Save Changes to All Files**  
We've changed four files, but we haven't saved any of them.  
##:argdo write  
>save all files in the argument list.  
  
##:wall  
>save all files in the buffer list, quicker to save all files.  
  
##:wnext  
>:write followed by :next  
  
#[Tip68](tip68.md) [Tip70](tip70.md)
