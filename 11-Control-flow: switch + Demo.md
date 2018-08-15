# Control-flow: switch + Demo

This can be used an alternative to if-else statement.

The Java switch statement executes one statement from multiple conditions. 

It is like if-else-if ladder statement. 

The switch statement works with byte, short, int, long, enum types, String and some wrapper types like Byte, Short, Int, and Long. Since Java 7, you can use strings in the switch statement.

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
