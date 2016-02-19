#Tip64: Record and Execute a Macro  
  
Vim offers more than one way to repeat changes. Dot and Macros.  
>dot is useful for repeating small changes.  
>macro is useful for repeating anything more substantial. We can **record** any number of keystrokes into a **register** and then play them back.  
  
Macros are ideal for repeating changes over a set of similar lines, paragraphs, or even files.  
There are two ways of executing a macro across a set of targets:  
>playing it back in series  
>running it multiple times in parallel  

Macros allow us to record a sequence of changes and then play them back.  
  
Many repetitive tasks involve making multiple changes. If we want to automate these, we can record a macro and then execute it.  
  
**Capture a Sequence of Commands by Recording a Macro**  
##q  
>q key functions both as the "record" button and the "stop" button.  
  
##q{register}  
>begin recording our keystrokes, giving the address of the register where we want to save the macro.  
  
##qa  
>begins recording and saves our macro into register a.  
>Then we make changes on the first line: ; var  
>press `q` to stop recording our macro.  
  
##:reg a  
>inspect the contents of register a.  
  
![tip64_1](images/tip64_1.png)  
  
**Play Back a Sequence of Commands by Executing a Macro**  
##@{register}  
>executes the contents of the specified register.  
  
##@@  
>repeats the macro that was invoked most recently.  
  
![tip64_2](images/tip64_2.png)  
  
**Execute the Macro in Series**  

**Execute the Macro in Parallel**  
  
Under the hood, Vim always executes macros **sequentially**, no matter which of these two techniques we use. The term in parallel is intended to draw an analogy with the robustness of parallel circuits. It is not meant to suggest that Vim executes multiple changes concurrently.  
  
#[Tip63](tip63.md) [Tip65](tip65.md)


