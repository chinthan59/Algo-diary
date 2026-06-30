# [Palindrome Number](https://leetcode.com/problems/palindrome-number/submissions/2051641899/)

---

## Approach: String Reversal

The solution involves converting the integer to a string and checking if it's equal to its reverse. This approach takes advantage of Python's slicing feature to reverse the string. The core insight is that a palindrome remains the same when its digits are reversed.

## Algorithm Steps
1. Convert the integer to a string
2. Reverse the string using slicing
3. Compare the original string with the reversed string

## Complexity
- **Time**: O(log n) because converting the integer to a string and reversing it takes time proportional to the number of digits in the integer, which is logarithmic in the size of the input
- **Space**: O(log n) because we're storing the string representation of the integer, which requires space proportional to the number of digits in the integer

## Patterns Used
`string manipulation` `reversal`

## Edge Cases
- Negative numbers are not palindromes because of the negative sign
- Single-digit numbers are always palindromes

## Alternative Approaches
- Reversing the integer mathematically without converting to a string
- Using a two-pointer approach to compare digits from the start and end of the string

## My Solution (python)
```python
1class Solution:
2    def isPalindrome(self, x: int) -> bool:
3        x=str(x)
4        if x==x[::-1]:
5            return True
6        else:
7            return False
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
