# Variable Scope

- Every variable has a ``SCOPE``

# Class level Variables
- Class level variable can be accessable entire class.
- This can't be assigned to variables declared before it.

  e.g.
  ```
  class variableScope{
    int i; // class level variable
    int j = i;
    void foo(){
      j = k;
    }
    j = k; // invalid because assigned to variables declared before it.
    int k;
  }
  
 # Scope of Local Variables
 
 -  A local variable is accessable from declaration point to end of block ``{...}``
    
    e.g.
    
    ```
    void foo(int p){
    ...
    ...
    int x = 0, z = x;
    if(x == 0){
      int y = x;
      int x = 0; // invalid as already declared. Re-declaration is not allowed.
    }
    y++; // invalid as out of scope.
    }
    ```
    
    # Shasowing Class-level Variables.
    - Class level variable will be hidden by a local level variable.
    
     e.g.
     
     ```
     int x = 10; //class-level
     
     void foo(){
     int x = 0; // shadows class variable x // local
     x++;
     this.x++; // class level variable
     }
     
     
     ```
    # Scope of Local Variable
    
    -  Methods invoked from current block will have new scope
    
    e.g.
    
    ```
    void foo(){
    ...
    
    int x = 0;
    bar();
    
    ...
    }
    
    void bar(){
    x++; // invalid 
    }
    ```
