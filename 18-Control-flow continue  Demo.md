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
# Invalid Lebeled Continue Statement

  e.g.
  ```
  x:if(){
   for(){
    for(){
      continue x; // invalid as continue is only applicable for loop statement.
    }
  }
  }
  ```
  
 ## DEMO 
 
 ```
 static void labeledContinue() {
	    System.out.println("\nInside labeledContinue ...");
	    int num = 0;
		
	    outermost: for (int i = 0; i < 10; i++) {
	        for (int j = 0; j < 10; j++) {    
	            if (i == 5 && j == 5) {
	                continue outermost;
	            }
	            num++;
	        }
	    }
		
	    System.out.println("num: " + num); // prints 55		
    }
 ```
