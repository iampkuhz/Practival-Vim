#Tip72: Tune the Case Sensitivity of Search Patterns  
  
We can tune the case sensitivity of Vim's search globally or on a per-search basis.  
  
**Setting Case Sensitivity Globally**  
We can make Vim's search patterns **case insensitive** by enabling the 'ignorecase' setting. But this setting has a side effect that influences the behavior of Vim's keyword autocompletion.  
  
**Setting Case Sensitivity per Search**  
>`\c`: causes the search pattern to **ignore case**.  
>`\C`: forces case sensitivity.  
  
**Enabling Smarter Default Case Sensitivity**  
##'smartcase'  
>If our pattern include an uppercase character, 'smartcase' canceling out the 'ignorecase'.  
>If our pattern include all lowercase, the search will be case insensitive.  
  
#[Tip71](tip71.md) [Tip73](tip73.md)
