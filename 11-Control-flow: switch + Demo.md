# Control-flow: switch + Demo

This can be used an alternative to if-else statement.

The Java switch statement executes one statement from multiple conditions. 

It is like if-else-if ladder statement. 

The switch statement works with **byte, short, int, long, enum types, String** and some wrapper types like Byte, Short, Int, and Long. Since Java 7, you can use **string** in the switch statement.

e.g.
```
switch(expression){    
case value1:    
 //code to be executed;    
 break;  //optional  
case value2:    
 //code to be executed;    
 break;  //optional  
......    
    
default:// This should not be a last block and can have break statement.     
 code to be executed if all cases are not matched;    
}    
```
## Switch Expression Type

- Integer, e.g. 7, x, x+y  **switch(int or String or enum)**
    - byte >> Byte
    - short >> Short
    - char >> Character 
    - int >> Integer
- String (Since Java 7)
- enum

## Case Label Restrictions
 - **The value of case level must be with-in the range of data type of switch expression.**
  
  e.g.
   ```
   public class SwitchDemo {
	public static void main(String[] args) {
		
		byte b = 1;
		switch(b) {
		
		case 1: 
				System.out.println("Case 1");
				break;
		
		case 2:
			System.out.println("Case 2");
			break;
			
			
		case 128: // this will throw compile time error as 128 is out side range of byte data type -128 to 127
			System.out.println("Case 128");
			break;
		}
	}
}
   ```

 - **The value of case level must be known at compile time.**
   
    e.g.
     ``` public class SwitchDemo {
     public static void main(String[] args) {
      byte ba = 2; //  final byte ba = 2 ; //will solve this compile time error.
      byte b = 1;
      switch(b) {

      case 1: 
        System.out.println("Case 1");
        break;

      case ba: // value is not known at compile time so it will throw compile time error.
       System.out.println("Case 2");
       break;


      case 3:
       System.out.println("Case 128");
       break;
      }
     }}
   ```

- **The case level value must be unique.**
   
   e.g.
     ```case 1: 
      System.out.println("Case 1");
      break;

    case 1: // Can't be duplicate.
     System.out.println("Case 2");
     break;

     ```
   

 - **The value of case level can't be null.**
   
   e.g.
   ```
   case 1: 
				System.out.println("Case 1");
				break;
		
		case null: // Can't be null.
			System.out.println("Case 2");
			break;
			
   
   ```
