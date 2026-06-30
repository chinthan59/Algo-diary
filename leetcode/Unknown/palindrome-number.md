# [Palindrome Number](https://leetcode.com/problems/palindrome-number/submissions/2051636611/)

---

## Approach: String Conversion

The solution involves converting the integer into a string to easily reverse and compare it. This approach simplifies the process of checking if the number is a palindrome. By comparing the string with its reverse, we can determine if the original number is a palindrome.

## Algorithm Steps
1. Convert the integer into a string
2. Reverse the string
3. Compare the original string with the reversed string
4. Return True if they are equal, False otherwise

## Complexity
- **Time**: O(log n) because converting the integer to a string and reversing the string both take time proportional to the number of digits in the number, which is log(n) for a number n
- **Space**: O(log n) as we are storing the string representation of the number, which requires space proportional to the number of digits in the number

## Patterns Used
`string manipulation` `reversal`

## Edge Cases
- Negative numbers are not palindromes because of the negative sign
- Single-digit numbers are always palindromes

## Alternative Approaches
- Mathematical approach: reversing the number without converting it to a string
- Two pointers approach: comparing characters from the start and end of the string

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
