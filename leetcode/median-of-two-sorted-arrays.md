# [Median Of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/description/)

---

## Approach: Binary Search

The problem can be solved by finding the partition point for both arrays such that elements on the left side of the partition point in both arrays are less than the elements on the right side. This can be achieved by using binary search to find the correct partition point. The key insight is to ensure that the total number of elements on the left side of the partition point is equal to the total number of elements on the right side.

## Algorithm Steps
1. Calculate the total length of both arrays
2. Determine which array is smaller to perform binary search on
3. Initialize the low and high pointers for the binary search
4. Perform binary search to find the correct partition point
5. Calculate the median based on the partition point

## Complexity
- **Time**: O(log(min(m, n))) where m and n are the lengths of the two input arrays, because we are performing a binary search on the smaller array
- **Space**: O(1) because we are only using a constant amount of space to store the partition points and the result

## Patterns Used
`binary search` `two pointers`

## Edge Cases
- When one or both of the input arrays are empty
- When the total length of the two arrays is odd or even

## Alternative Approaches
- Merging the two sorted arrays and then finding the median, which has a time complexity of O(m + n)
- Using a heap data structure to find the median, which has a time complexity of O(m + n) log(m + n)

## My Solution (python)
```python
-106 <= nums1[i], nums2[i] <= 106
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
