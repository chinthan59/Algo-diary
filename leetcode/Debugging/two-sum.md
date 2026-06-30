# [Two Sum](https://leetcode.com/problems/two-sum/submissions/2051657805/)

---

## Approach: Brute Force

The solution iterates over the list of numbers and checks every pair of numbers to see if their sum equals the target. This approach is straightforward but not efficient for large lists. It relies on the basic concept of comparing each element with every other element in the list.

## Algorithm Steps
1. Initialize two pointers, one at the start of the list and one at the next element
2. Compare the sum of the numbers at the current pointers with the target
3. If the sum equals the target, return the indices of the two numbers
4. If not, move the second pointer to the next element and repeat the comparison
5. If no pair of numbers adds up to the target after checking all pairs, return an empty list

## Complexity
- **Time**: O(n^2) because it uses two nested loops to compare each pair of numbers in the list
- **Space**: O(1) because it only uses a constant amount of space to store the indices of the two numbers that add up to the target

## Patterns Used
`brute force` `nested loops`

## Edge Cases
- An empty list
- A list with only one element
- A list with duplicate numbers
- A list with negative numbers

## Alternative Approaches
- Using a hash map to store the numbers and their indices, allowing for a single pass through the list and a time complexity of O(n)
- Sorting the list first and then using a two-pointer technique to find the pair of numbers

## My Solution (python)
```python
1class Solution:
2    def twoSum(self, nums: List[int], target: int) -> List[int]:
3
4
5        # Compare every element with all subsequent elements
6        for i in range(len(nums)):
7            for j in range(i + 1, len(nums)):
8                if nums[i] + nums[j] == target:
9                    return [i, j]
10        return []
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
