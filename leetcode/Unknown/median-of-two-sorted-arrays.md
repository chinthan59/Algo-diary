# [Median Of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/submissions/2051659358/)

---

## Approach: Merging and Sorting

The solution involves merging the two input arrays into a single array and then sorting it to find the median. The core insight is that the median of the combined array can be found by looking at the middle element(s) after sorting. This approach ensures that the solution is straightforward but may not be the most efficient for large inputs.

## Algorithm Steps
1. Merge the two input arrays into a single array
2. Sort the merged array in ascending order
3. Determine the length of the merged array
4. Find the middle index of the merged array
5. If the length of the merged array is even, return the average of the two middle elements
6. If the length of the merged array is odd, return the middle element

## Complexity
- **Time**: O((m+n)log(m+n)) because the sorting operation dominates the time complexity, where m and n are the lengths of the input arrays
- **Space**: O(m+n) because a new array is created to store the merged and sorted elements

## Patterns Used
`merging` `sorting`

## Edge Cases
- When one or both of the input arrays are empty
- When the input arrays have different lengths
- When the input arrays contain duplicate elements

## Alternative Approaches
- Using a binary search approach to find the median without sorting the entire array
- Using a heap data structure to efficiently find the median

## My Solution (python)
```python
1class Solution:
2    def findMedianSortedArrays(self, nums1, nums2):
3        new=[]
4        new.append(nums1)
5        new.append(nums2)
6        new=[item for sublist in new for item in sublist]
7        new=sorted(new)
8        n=len(new)
9
10        m=len(new)//2
11        if n%2==0:
12            return (new[m]+new[m-1])/2
13        else:
14            return new[m]
15
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
