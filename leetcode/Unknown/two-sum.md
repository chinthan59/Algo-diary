# Two Sum

**Platform**: leetcode | **Difficulty**: Unknown | **Language**: python
**Runtime**: Problem ListProblem ListDebugging...Submit-0StreaksExtend Your Streak!00:00:00Chinthan K MAccess all features with our Premium subscription!My ListsNotebookProgressPointsTry New FeaturesOrdersMy PlaygroundsSettingsAppearanceAppearanceSystem DefaultLightDarkSign OutSystem DefaultLightDarkPremiumDescriptionDescriptionAcceptedAcceptedEditorialEditorialSolutionsSolutionsSubmissionsSubmissionsCodeCodeTestcaseTestcaseTest ResultTest Result All SubmissionsAccepted63 / 63 testcases passedChinthan K Msubmitted at Jul 01, 2026 00:30AnalysisSolutionCreated with Highcharts 11.1.018ms769ms1519ms2269ms0%25%50%75%
                  
                Created with Highcharts 11.1.018ms769ms1519ms2269msCodePython31class Solution:
2    def twoSum(self, nums: List[int], target: int) -> List[int]:
3
4
5        # Compare every element with all subsequent elements
6        for i in range(len(nums)):
7            for j in range(i + 1, len(nums)):
8                if nums[i] + nums[j] == target:
9                    return [i, j]
10        return []View more 0/5Ln 1, Col 1You must run your code firstFindHeaderBarSizeFindTabBarSizeFindBorderBarSize | **Memory**: Chinthan K M
**URL**: https://leetcode.com/problems/two-sum/submissions/2051607661/

---

## Approach: Brute Force

The solution involves checking every possible pair of elements in the list to see if their sum equals the target. This approach is straightforward but not efficient for large lists. It relies on the basic concept of comparing each element with every other element to find a pair that meets the condition.

## Algorithm Steps
1. Initialize two nested loops to compare each element with every other element in the list
2. For each pair of elements, check if their sum equals the target
3. If a pair is found whose sum equals the target, return their indices
4. If no such pair is found after checking all elements, return an empty list

## Complexity
- **Time**: O(n^2) because for each element in the list, we are potentially checking every other element
- **Space**: O(1) because we are not using any additional space that scales with input size, excluding the space needed for the output

## Patterns Used
`brute force` `nested loops`

## Edge Cases
- An empty list or a list with a single element should return an empty list because there are not enough elements to form a pair
- If there are duplicate pairs that sum to the target, this solution will return the first one it encounters
- If the list contains negative numbers or zero, the solution still works as expected

## Alternative Approaches
- Using a hash map to store the elements we have seen so far and their indices, allowing for a single pass through the list and a significant reduction in time complexity
- Sorting the list first and then using a two-pointer technique to find the pair, though this would require additional space for sorting and would not preserve the original indices

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
