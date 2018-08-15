# Bit Shift Operators

1. Like Bitwise operator Bit Shift operator also work with individual bits of its operand. 
2. Bit Shift operator simply shift bits.
3. Its only applicable on integer primitives.
4. This can only shift the bits either left or right direction.

## Three Bit Shift Operators
1. << -- Left-shift
2. \>\>\> -- Unsigned Right-shift
3. \>\> -- Signed right-shift

### Left-shift Operator (<<)

1. Its a binary operator and its left shifts left operand by the number of bit specified on right. 
2. Let x = 6, y = 1
> Result (x << y) --> 12
3. Inserts zeroes at lower-order bits position.  00000000 00000000 00000000 0000 __0 1 1 0__ **<--- lower order bit position**
4. Same as multiplication by powers of 2
    e.g. 6 << 1 ---> 6 * 2^1 --> 12
         8 << 2 ---> 8 * 2^3 --> 32
#### Explanation:
    00000000 00000000 00000000 0000 0 1 1 0 (X--6)
    00000000 00000000 00000000 0000 1 1 0 0 (Result Shiftd 1 bit to left. ** 6 << 1 **)
> As you can see the last digit 110 (6) has been shifted left operand to (1)

> So as a result  00000000 00000000 00000000 0000 1 1 0 **0** ( **As bit shifted to left newly value filled with 0 at lower order bit position**) 
 
### Unsigned Right-shift Operator (>>>)

1. Its a binary operator and its right shifts left operand by the number of bit specified on right. 
2. Let x = 12, y = 1
> Result (x >>> y) --> 6
3. Inserts zeroes at higher-order bits position. **Higher order bit position -->** __00000000__ 00000000 00000000 0000 0 1 1 0
4. Same as division by powers of 2
    e.g. 12 >>> 1 ---> 12 / 2^1 --> 6
         8 >>> 2 ---> 8 / 2^2 --> 2
#### Explanation:
    00000000 00000000 00000000 0000 1 1 0 0 (X--12)
    00000000 00000000 00000000 0000 0 1 1 0 (Result Shiftd 1 bit to right. ** 12 >>> 1 **)
> As you can see the last digit 1110 (12) has been shifted left operand to (1)

> So as a result **0**0000000 00000000 00000000 0000 0 1 1 0 

( **As bit shifted to right newly value filled with 0 at higher-order bits position**) 



### Signed Right-shift Operator (>>)

1. Its a binary operator and its right shifts left operand by the number of bit specified on right. 
2. Same as Unsigned Right Shift Operator (>>>), But padded with MSB (Most Significant Bits)
3. Sign is preserved.
4. Inserts one at higher-order bits position. **Higher order bit position -->** __11111111__ 00000000 00000000 0000 0 1 1 0
5. Same as division by powers of 2

    e.g. -2147483552 >> 4 ---> 2147483552 / 2^4 --> -134217722
  
#### Explanation:
    10000000 00000000 00000000 01100000 (-2147483552)
    11111000 00000000 00000000 00000110 (Result Shiftd 1 bit to right. ** 2147483552 >> 4 **)
> As you can see the last digit 1100000 (-2147483552) has been shifted left operand to (4)

> So as a result **11111**000 00000000 00000000 00000110 

( **As bit shifted to right newly value filled with 1 at higher-order bits position**) 
