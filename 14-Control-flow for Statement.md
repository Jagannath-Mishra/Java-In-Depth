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
