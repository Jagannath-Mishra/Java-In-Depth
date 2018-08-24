# Control-flow while Statement
- Another Iteration statement.
- This while loop is also known as ``Entry Control Loop``. i.e. its check condition first before starting of iteration.
- We must use ``for`` loop iff number of iteration is known.
- We must use ``while`` loof iff number of iteration is unknown. 
- While loop has only condition-expression
  e.g.
  
    ```
    while(condition-expression){
    // do something;
    }
    ```
    
# Control-flow do-while Statement

- Another Iteration statement and its runs at least once
- This while loop is also known as ``Exit Control Loop``. i.e. its check condition after first iteration completes.
  e.g.
  
    ```
    int input = 0;
    
    do{
      input =  getUserInput();
    }while(input <= 0)
    // Perform some action
    
    ```
    
    # Infinite Loop
    
   - Loop which iterate forever.
   - For infinite loop while loop is preferable but other then infinite loop concept for loop is preferable. 
   
   e.g.
   ```
   while(true){
   // do something
   }
   
   
   for(;;){
   // do something
   }
   
   do {
    // do something
   }while(true)
   ```
