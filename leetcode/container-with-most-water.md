# [Container With Most Water](https://leetcode.com/problems/container-with-most-water/description/)

---

## Approach: Two Pointers

The core insight behind this solution is to use two pointers, one starting from the beginning and one from the end of the array, and move them towards each other. The area between the two pointers is calculated at each step, and the maximum area found so far is updated. The pointer with the smaller height is moved towards the other pointer because moving the pointer with the larger height wouldn't increase the area.

## Algorithm Steps
1. Initialize two pointers, one at the beginning and one at the end of the array
2. Calculate the area between the two pointers
3. Update the maximum area if the current area is larger
4. Move the pointer with the smaller height towards the other pointer
5. Repeat steps 2-4 until the two pointers meet

## Complexity
- **Time**: O(n), where n is the number of lines, because each line is visited at most once
- **Space**: O(1), because only a constant amount of space is used to store the pointers and the maximum area

## Patterns Used
`two pointers` `greedy`

## Edge Cases
- If the input array is empty, return 0
- If the input array has only one element, return 0
- If the input array has two elements, return the minimum of the two elements

## Alternative Approaches
- Brute force approach: calculate the area for all possible pairs of lines and return the maximum area
- Dynamic programming approach: not applicable for this problem

## My Solution (python)
```python
// Could not extract code. Please make sure the code editor is visible.
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
