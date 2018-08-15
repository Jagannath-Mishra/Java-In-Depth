# Bitwise Operators + Demo

#### As the name suggest Bitwise Operators are operated on individual bit of operands.

###### Operands:
1. Integer Primitives - Operand promotion rule applies. ( operator smaller the int automatically promoted to int)
2. Boolean (very rarely used)
3. Bitwise operator always work at **bit** level.
4. This operator represent the binary representation of integer operand then operate them at bit level.

## Where Bitwise Oprators are used. 

1. Used mostly in embedded system. Which works on resource constraint environment
2. In embedded environment we may work with very limited memory. 
3. Also used in Hashtable e.g. HashMap's hash function.
4. Heavly used in data compression adn data encryption. 

###### NOTE: Generally we may never use Bitwise operator unless we are doing really low level programming work where performance is critical and things has to be managed very efficiently.


## How Bitwise Operator works.
#### Four Bitwise Operator
1. & ---> Bitwise AND
2. | ---> Bitwise OR
3. ^ ---> Bitwise XOR (Exclusive OR)
4. ~ ---> Bitwise NOT


## Bitwise AND (&)

1. Bitwise AND (&) operator returns 1 if both input bits are 1
2. Let x = 1, y = 3

> Result (x&y) --> 1

#### Explanation:
    00000000 00000000 00000000 000000 0 1 (X)
    00000000 00000000 00000000 000000 1 1 (y)
    00000000 00000000 00000000 000000 0 1 (Result)
> As you can see the last digit 1(x) 1(y) = 1 and 0(x) 1(y) = 0 (**where true = 1 & false = 0**)


## Bitwise OR (|)

1. Bitwise OR (|) operator returns 1 if either of input bits is 1
2. Let x = 1, y = 3
> Result (x|y) --> 3

#### Explanation:
    00000000 00000000 00000000 000000 0 1 (X)
    00000000 00000000 00000000 000000 1 1 (y)
    00000000 00000000 00000000 000000 1 1 (Result)
> As you can see the last digit 1(x) 1(y) = 1 and 0(x) 1(y) = 1 (**where true = 1 & false = 0**)



## Bitwise XOR (^)

1. Bitwise XOR (^) operator returns 1 if only one of the input bits is 1, but not both if both of the bits are 1 then it's return 0.
2. Let x = 1, y = 3
> Result (x^y) --> 2

#### Explanation:
    00000000 00000000 00000000 000000 0 1 (X)
    00000000 00000000 00000000 000000 1 1 (y)
    00000000 00000000 00000000 000000 1 0 (Result)
> As you can see the last digit 1(x) 1(y) = 0 and 0(x) 1(y) = 1 (**where true = 1 & false = 0**)

## Bitwise NOT (~)

1. Bitwise NOT (~) is a **Unary** operator which inverts bits.
2. Let x = 1
> Result (~X) --> -2

#### Explanation:
    00000000 00000000 00000000 000000 0 1 (X)
    11111111 11111111 11111111 111111 1 0 (Result)
> As you can see the all  digita 1(x)  = 0 and 0(x)  = 1 (**where true = 1 & false = 0**)

## Non Short Circuit Operators

1. & and | operator are refered as non short circuit Operator.
   i.e. This operator force to check both the operands (right operand always evaluated even if left operand evaluated to false)
2. Always check both side of the operand. 


## Compound Bitwise Assignment

1.  operand1 = operand1 & operand2

    i.e. operand1 &= operand2 (**Compound way to write bitwise operator**)
    
    e.g., boolean b = true;
          b &= false; // Assigns false value to b.
2.  operand1 |= operand2
3.  operand1 ^= operand2

```
public class BitwiseOperator {

	public static void main(String[] args) {
		int x = 1;
		int y = 3;
		
		System.out.println("X & Y : " + (x & y)); //1
		System.out.println("X | Y : " + (x | y)); //3
		System.out.println("X ^ Y : " + (x ^ y)); //2
		
		System.out.println("X  : " + (~ x )); // -2
		
		char c1 = 'a'; 
		char c2 = 'B';
		
		System.out.println("c1 | c2 : " + (c1|c2)); //99
		
		// Since bitwise operator only work on Integer types, following will not compile.
		
		double d1 = 3.14;
		float f1 = 5.14f;
		//System.out.println("d1 | d2: " + (d1 | f1)); // Compilation error: The operator | is undefined for the argument type(s) double, float
	}
}
```
