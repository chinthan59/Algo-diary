# [Palindrome Number](https://leetcode.com/problems/palindrome-number/submissions/2051675084/)

---

## Approach: String Manipulation

The solution involves converting the integer into a string and checking if it's the same when reversed. This approach takes advantage of Python's slicing feature to easily reverse the string. The core insight is that a palindrome reads the same backward as forward.

## Algorithm Steps
1. Convert the integer to a string
2. Compare the string with its reverse
3. Return True if they're the same, False otherwise

## Complexity
- **Time**: O(log n) because converting the integer to a string and reversing the string both take time proportional to the number of digits in the integer, which is logarithmic in the size of the integer
- **Space**: O(log n) because we're storing the string representation of the integer, which requires space proportional to the number of digits in the integer

## Patterns Used
`string manipulation` `reversal`

## Edge Cases
- Negative numbers are not palindromes because of the negative sign
- Single-digit numbers are always palindromes

## Alternative Approaches
- Reversing the integer mathematically without converting to a string
- Using a two-pointer approach to compare characters from the start and end of the string

## My Solution (python)
```python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        x=str(x)
        if x==x[::-1]:
            return True
        else:
            return False

```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
