# Control-flow continue Statement
  
  - This used with only loops ( for / while / do-while )
  - Continues with the next iteration of innermost loop.
    e.g.
    
      ```
      while (condition){
        if(condition){ // if this if conditon is ture then rest of the while loop will be skipped and start with next iteration.
          continue;
        }
      }
      ```
## Invalid Example

  ```
   if(){
    continue; // invalid as contiune is only applicable for loop statement.
   }
  ```
  
# Lebeled Continue Statement

- This is same as Lebeled Break statement but only applicable for loops.
  
  e.g.
  ```
  x:for(){
    for(){
      continue x;
    }
  }
  ```
