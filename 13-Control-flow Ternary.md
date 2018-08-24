# Control-flow Ternary

- This Ternary statement can be used as shorthand for if-else statement with single statement. 
- result = (boolean-expression) ? true-expression : false-expression;
- Similar if-else statement.
  e.g.
  ```
    if (boolean-expression){
      result = true-expr;
    }
    else{
      result = false-expr;
    }
  ```
## When is Ternary Preferred?
- To constructs smart string : e.g. greeting =  "hello " + (user.isMale())? "Mr. ":"Ms. ");
- Logging smart string : e.g. System.out.println("Jaga is " + (s.isMale() ? "male" : "female")); 

> This can't be expressed as an expression statement. 
  
 
 e.g.
  ```
  (boolean-expr)?true:false;  // invalide not part of expression statement.
  
  boolean result = (boolean-expr)?true:false; // valide
  
  boolean foo(){
  return (boolean-expr)?true:false; // valide 
  }
  
  ```
