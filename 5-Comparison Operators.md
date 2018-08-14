# Comparison Operators

This operator is used to compare one operand with another operand. This operator typically used in control flow statements.
  - e.g. x > y  ( Comparison  is happening between x and y operand)
  - This operator always test some condition like x>y, x==y and x<y and so on..
  - This operator always generate a **boolean** value. 
  - if(x > y) { ----- };
 
 ## Comparison Operators Usages 
 
 #####  |   Operator ==   | Description:   equal to |  e.g. (let x = 5 ) x == 7 ---> false | Primitive Support   (All Type)|
 #####  |   Operator >    |   Description: greater than |  e.g. (let x = 5 ) x > 7 ---> false | Primitive Support  (Not for Boolean Type) |
 #####  |   Operator <    |   Description: less than |  e.g. (let x = 5 ) x < 7 ---> true | Primitive Support  (Not for Boolean Type) 
 #####  |   Operator >=    |   Description: greater than and equal |  e.g. (let x = 5 ) x >= 7 ---> false | Primitive Support  (Not for Boolean Type) 
 #####  |   Operator <=    |   Description: less than and equal |  e.g. (let x = 5 ) x <= 7 ---> true | Primitive Support  (Not for Boolean Type) 
 #####  |   Operator ==   | Description:   equal to |  e.g. (let x = 5 ) x != 7 ---> ture | Primitive Support   (All Type)|


## Object Reference Comparison 

  ```
    Student s1 = new Student(); // s1  is referancing one student object
    Student s2 =  new Student(); // s1  is referancing one student object
    
    if(s1==s2) // false
    {
     System.out.print("Both object are referancing to different memory address.");
    }
    
     if(s1!=s2) // true
    {
     System.out.print("Both object are not referancing to different memory address.");
    }
  
  ```
  ##### Typical Operation: objRef == null or objRef != null
   
   ```
    boolean foo(Student s){
      if (s == null){ // This reference check will prevent serious and embracing errors at run time.
        return false;
      }
      return true;
    }
   ```
