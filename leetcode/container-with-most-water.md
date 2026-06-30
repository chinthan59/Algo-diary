# [Container With Most Water](https://leetcode.com/problems/container-with-most-water/submissions/2051677586/)

---

## Approach: Two Pointers

The solution uses two pointers, one at the start and one at the end of the array, to track the maximum area that can be trapped between two lines. The area is calculated as the minimum height of the two lines multiplied by the distance between them. The pointers are moved based on the height of the lines to maximize the area.

## Algorithm Steps
1. Initialize two pointers, one at the start and one at the end of the array
2. Calculate the area between the two lines and update the maximum area if necessary
3. Move the pointer of the shorter line towards the other pointer
4. Repeat steps 2-3 until the pointers meet

## Complexity
- **Time**: O(n), where n is the number of lines, because each line is visited at most once
- **Space**: O(1), because only a constant amount of space is used to store the pointers and the maximum area

## Patterns Used
`two pointers` `greedy`

## Edge Cases
- When the input array is empty
- When the input array has only one element
- When the input array has two elements of the same height

## Alternative Approaches
- Brute force approach: calculate the area for all possible pairs of lines and return the maximum area
- Dynamic programming approach: store the maximum area for each subarray and use it to calculate the maximum area for the entire array

## My Solution (python)
```python
1class Solution:
2    def maxArea(self, height):
3        left, right = 0, len(height) - 1
4        max_water = 0
5        
6        while left < right:
7            width = right - left
8            max_water = max(max_water, min(height[left], height[right]) * width)
9            
10            if height[left] < height[right]:
11                left += 1
12            else:
13                right -= 1
14        
15        return max_water
16
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
