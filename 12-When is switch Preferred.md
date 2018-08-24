# When is switch Preferred

- Readablity improved.
- Intent
   -  By using a switch programer deliberately states that only one variable is involved.
   e.g.
    ```
    switch(code) // here code variable is only one variable which deals with entire control flow.
    ```
- Speed
  - Faster due to single condition & constant case lables.
  - if # condition is N, then if is O(N) linner time and switch is O(1) constant time.
  - if # condition > 100, if to switch conversion is on longer micro-optimization >> use profiler like **J-profiler** 
  
  > Profiler - is used to analyze the perfermance of the code. 
