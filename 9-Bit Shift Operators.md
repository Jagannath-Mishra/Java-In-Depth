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
3. Inserts zeroes at lower-order bits position.
4. Same as multiplication by powers of 2
    e.g. 6 << 1 ---> 6 * 2^1 --> 12
         8 << 2 ---> 8 * 2^3 --> 32
#### Explanation:
    00000000 00000000 00000000 0000 0 1 1 0 (X--6)
    00000000 00000000 00000000 0000 1 1 0 0 (Result Shiftd 1 bit to left. ** 6 << 1 **)
> As you can see the last digit 110 (6) has been shifted left operand to (1)

> So as a result 110**0** ( **As bit shifted to left newly value filled with 0**) 
 
### Unsigned Right-shift Operator (<<)

1. Its a binary operator and its right shifts left operand by the number of bit specified on right. 
2. Let x = 12, y = 1
> Result (x >>> y) --> 6
3. Inserts zeroes at higher-order bits position.
4. Same as division by powers of 2
    e.g. 6 << 1 ---> 6 / 2^1 --> 12
         8 << 2 ---> 8 / 2^3 --> 32
#### Explanation:
    00000000 00000000 00000000 0000 1 1 0 0 (X--12)
    00000000 00000000 00000000 0000 0 1 1 0 (Result Shiftd 1 bit to right. ** 12 >>> 1 **)
> As you can see the last digit 1110 (12) has been shifted left operand to (1)

> So as a result **0**110 ( **As bit shifted to left newly value filled with 0 at higher-order bits position**) 
