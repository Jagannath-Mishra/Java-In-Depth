

# Arithmetic Operation Rules
### Opertor Precedence
1. Multiplicative operators ( \*, /, %) have higher preedence over additive operators (+,-).
   - e.g. 5 + 9 + 3 +( 2 * 5 )
2. Operators in same group are evaluated left to right.
   - e.g. 5 + 9 - 3 +( 2 * 5 )  // 5 + 9 will added first then subsctracted from 3 then added to 2 \* 5 
3. Use paranthesis to change the order of evaluation.
   - e.g. ((5 + (9 - 3)) + ( 2 * 5 ) // Here we are forcing operator to evaluate by our order.
   
### Operand Promotion Rules
1. Operands smaller then int are promoted to int.  (byte, short and char  are promoted to int )
      - e.g. 127 (byte) + 1 (byte) --> 127 (int) + 1 (int) --> 128 (int)
      - e.g. 'a' (char) + 'b' (char) --> 97 (UTF-16) + 98 (UTF-16) --> 195 (int)
### Same-Type Operations Rules
If both operands are of same type that is int, long, float or double, then operaions are carried in the type and evaluated to a value of that type

e.g. 5 + 6 = 11

1/2 = 0 , _actually it should be 0.5_

### Mixed-Type Operations Rules
If both operands are belongs to differnet type, then smaller type is automatically promoted to larger type.
   ##### Order of Promotion _ int --> long --> float --> double _
   e.g. 1/2 or 1.0/2 --> (automatically converted ) 1.0/2.0 ---> 0.5 
   e.g. char + float ---> ( char will automatically coverted to int ) int + float --> (again int will further converted into float ) float + float ---> float
   
   
   e.g. 9/5*20.1 ---> (9/5)* 20.1 --> 1*20.1  ----> 1.0 *20.1 ---> 20.1 
   
   ### Code Demonstration
   ```
   static void charTypePromotion() {
	  System.out.println("\nInside charTypePromotion ...");
	  char char1 = 50; // Will be assigned corresponding UTF16 value 2
	  System.out.println("char1: " + char1); 
	  System.out.println("(73 - char1): " + (73 - char1)); // char1 gets promoted to int, i.e., decimal equivalent 50 in UTF16 is used	  
	  System.out.println("(char1 - '3'): " + (char1 - '3')); // char1 & '3' are promoted to ints	
	  System.out.println("('a' + 'b'): " + ('a' +'b')); // 'a' & 'b' are promoted to ints and the respective equivalents 97 & 98 are added
    }
   ```
