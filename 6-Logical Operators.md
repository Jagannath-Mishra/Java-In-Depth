# Logical Operators

Logical operator are used to test multiple condition. 

e.g. 
```
if(a>b && b>c){
  do something
}
```

## Type of Logical operator
  
  **Operator ------------- Name--------------e.g. (let x = 5, y = 6)**
 
 &&----------------------AND------------------((x<7) && (y<3)) --> false
 
 ||----------------------OR------------------((x<7) || (y<3)) --> ture
 
 !----------------------NOT------------------!(x<7) --> false
 
  
 ## Additional Facts about Logical Operators
 
 1. This operator test one or more condition 
 2. e.g. if((x<7) && (y<3) &&(z>5)) {...........}
 3. Generates boolean value.
 4. Basically this operator used in control-flow statements
 5. Also called as conditional operator.
  
## Short Circuit Operators

Logical AND (&&) and Logical OR (||) are also called short circuit operators.

1. && and || 
    - && 
        - if left operand is false, then entire expression return false.
        - if left operand is true, then right operand still evaluated.
    - ||
        - if left operand is true, then entire expression return ture.
    -  && 
        - This AND Operator Prevets NullPointerException 
          e.g. : if(**s != null** && s.getGender()=="male")
      
 ```
  int a =2;
	int b = 3;
	int c = 4;
	if( a == 3 && b == 4 || c == 4 ) {
		System.out.println("Java...!");  // Java...!
	}
  ```
