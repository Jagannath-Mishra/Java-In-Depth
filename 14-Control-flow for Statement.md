# Control-flow for Statement

A for is tipically used to iterate or loop over elements of an array or similar data sturcture and do something on each element.

## for Statement
  
  - example:
  ```
      int[] iarr = {0,1,2,3,4,5,6,5,4,5};
      
      for(int i = 0; i<iarr.lenght;i++){
      System.out.println(iarr[i]);
      }
```

#### Iteration 1:  i = 0    0 < 10    print 0  i = 1
#### Iteration 2:           1 < 10    print 1  i = 2

> Note: Initilization expression **(int i = 0)** will execute once and rest condition exp and increment expession runs multiple times.

## Initialization ~ Optional

- Initialization part is optional
    ```
    int[] iarr = {0,1,2,3,4,5,6,5,4,5};
    int i = 0;  
      for(/*Opetional*/; i<iarr.lenght;i++){
      System.out.println(iarr[i]);
      }
    ```
## Initialization ~ Declaration Statement

  - for(int i = 0 ; ; ) // Valid Declaration
  - for(int i = 0, j = 1 ; ; ) // Valid Declaration
  - for(int i = 0, int j = 0 ; ; ) // **In-Valid Declaration**
  - for(int i = 1, double d = 1.0 ; ; )  // **In-Valid Declaration**
  - for(i++;;) // Valid
  - for(i = 1, double d = 1.0 ; ; )// **In-Valid Declaration**
  - for(System.out.println(i);;) // Valid
  - for(System.out.println(i),i++;;) // Valid
  
## Condition ~ Expression

  - Must be evalute to boolean value.
  - This statement is optional 
    - If Omitted, a true is assumed by default. i.e. infinite loop
    
      ```
      for(int i =0; ; i++){
      // Infinite loop as condition statement is omitted.
      }
      ```
  - In condition expression we can only provide boolean statement, no other datatype other than boolean is accepted. 
    e.g.
      ```
      for(int i =0; 1 ; i++){
      // 1 is a int value so it will throw compile time error
      }
      
       for(int i =0; true ; i++){
      // true is a boolean value so it will accepted.
      }
      ```
  ## Expression ~ Increment/Decrement List
  
  - We can have list of comma-separated expression statements.
  
    e.g. 
      ```
        for(int = 0; i<arr.length; System.out.println(arr[i]),i++);
      ```
