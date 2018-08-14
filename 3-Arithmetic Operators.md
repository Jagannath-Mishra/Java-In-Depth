# Arithmetic Operators
1. Addition( + )
   - int i = 5 + 2; ( Unary Plus: i = +5  or i = -41)
   - string concatination ( "abc"+"xyz" )
2. Substraction( - )
   - int i = 5 - 2; ( Unary Minus: i = -10)
3. Multiplication (\*)
   - int i = 5 * 2
4. Division (/)
   - int i = 5 / 2
5. Modulus(%)
   - int i = 5 % 2 // i = 1
6. Pre or Post Increment (++)
   - e.g. int x = 5;
   - int y = x++; // y = 5, x = 6 ( Y is first assing the current value of x (5) and its incremented to x as 6 )
   - int y = ++x; // y = 6, x = 6 ( Y is first increment the current value of x (6) and its assign to y as 6 and x as 6 )
7. Pre or Post Decrement (--)
   - e.g. int x = 5;
   - int y = x++; // y = 5, x = 4 ( Y is first assing the current value of x (5) and its assign to y as 6 )
   - int y = ++x; // y = 4, x = 4 ( Y is first decrement the current value of x (4) and its assign to y as 4 and x as 4 )
###### Note: Arithematic operator are only applicabe for premitive numaric types. That is they accept all premitive type except boolean.

## Compound Arithematic Assignment Operators
 This provides a shot syntax for assigning the result of the arithematic variable to some variable. 
 
 e.g.  x = x + 5;
 
 Rewrite :  x += 5;
 
 =+ will be treated as only assignment operation.

Similarly: -=, +=, /= and %=

## Arithmetic Operation Rules
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
