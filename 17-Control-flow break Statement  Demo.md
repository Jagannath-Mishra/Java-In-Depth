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
  # Lebeled break Statements
  
  - When we want to exist from outter most loop instade of innermost loop then we must use lebeled break statement. 
  - lebel: block statement.
  ### What is block statement.
      1. 0 or more statement in curly braces.
      2. e.g. control-flow statements, initilizers
         ```
         if(){ // block 1
          }else{ // block 2
          }
        
        ```
      3. Statements are executed sequentially.
      4. Can be nested.
      
   ## Valid lebeled-break statement.
   - Example - 1
    ```
    x: if(){
      break x ;
    }
    ```
    - Example - 2
    
    ```
   outermost: for (int i = 0; i < 10; i++){
        for (int j = 0; j < 10;  j++{
          if (i == 5 && j == 5){
            break outermost;
          }
          num++;
        }
    }
   System.out.print("num: "+num);// num : 55
    ```
  ## In-valid lebeled-break statement.
  ```
  lebel1: for(){
    for(){
      break lebel1; // Accepted  
    }
  }
  
  
  lebel2: for(){
    for(){
      break lebel1; // compiler error as lebel1 is not in scope.
    }
  }
  ```
  
