# [Palindrome Number](https://leetcode.com/problems/palindrome-number/description/)

---

## Approach: Mathematical Conversion

The solution involves converting the integer into a string to easily check if it's a palindrome. This approach takes advantage of Python's slicing feature to reverse the string and compare it with the original. The core insight is that a palindrome reads the same backward as forward.

## Algorithm Steps
1. Convert the integer into a string to easily access and compare its digits
2. Compare the string with its reverse to check if it's a palindrome
3. Return True if the string is the same when reversed, False otherwise

## Complexity
- **Time**: O(log(n)) because converting an integer to a string in Python takes logarithmic time with respect to the number of digits in the integer
- **Space**: O(log(n)) as we are storing the string representation of the integer, which requires logarithmic space with respect to the number of digits in the integer

## Patterns Used
`string manipulation` `palindrome check`

## Edge Cases
- Negative numbers cannot be palindromes because of the negative sign
- Single-digit numbers are always palindromes
- The input range -231 <= x <= 231 - 1 is within the range of a 32-bit signed integer

## Alternative Approaches
- Reversing the integer mathematically without converting to a string, which would also be O(log(n)) in time but might be more efficient in practice due to avoiding string operations
- Using a two-pointer approach with the string, starting from both ends and moving towards the center

## My Solution (python)
```python
-231 <= x <= 231 - 1
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
