# Control-flow break Statement

- Exits immediately enclosing switch or loop (for/while/do-while) statement.
  e.g.
    ```
    
    for(){
    break;
    }
    //exits for
    
    
    for(){
    if(){ 
      break;
    }
    // exits for if if conditon is true.
    }
    
    for(){
      for(){
        break;
      }
      // exits inner for loops 
    }
    
    for(){
      switch(){
        case: break;
      }
      //exist switch
    }
    
    ```
    
    ## Invalid break statement.
     - ``break`` statement must be with in the loop or switch statement other wise it will throw a compile error.
      e.g.
      
      ```
      if(a>b){
      break; //  compile time error;
      }
      ```
    
