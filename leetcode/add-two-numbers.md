# [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/submissions/2051669128/)

---

## Approach: Two Pointers

The solution utilizes a two-pointer technique to traverse both linked lists simultaneously, adding corresponding nodes and handling any carry-over values. This approach allows for efficient processing of the input lists. The use of a dummy node simplifies the code by avoiding special handling for the head of the result list.

## Algorithm Steps
1. Create a dummy node to simplify the code and avoid special handling for the head of the result list
2. Initialize two pointers, one for each input linked list, and a carry variable to track any overflow
3. Traverse both linked lists, adding corresponding nodes and updating the carry variable as necessary
4. Create new nodes for the result linked list, using the sum of the current nodes and the carry value
5. Return the next node of the dummy node, which is the head of the result linked list

## Complexity
- **Time**: O(max(m, n)) where m and n are the lengths of the input linked lists, as we process each node exactly once
- **Space**: O(max(m, n)) for the result linked list, as in the worst case, the result list can be one node longer than the longer input list

## Patterns Used
`two pointers` `linked list`

## Edge Cases
- Input lists of different lengths
- Input lists with a carry-over value at the end
- Input lists with all zeros

## Alternative Approaches
- Using recursion to add the linked lists, which would have a higher space complexity due to the recursive call stack
- Converting the linked lists to integers, adding them, and then converting back to a linked list, which would have a higher time complexity due to the conversion steps

## My Solution (python)
```python
1class Solution:
2    def addTwoNumbers(self, l1, l2):
3        dummy = ListNode(0)
4        curr = dummy
5        carry = 0
6
7        # Traverse both lists
8        while l1 or l2 or carry:
9            val1 = l1.val if l1 else 0
10            val2 = l2.val if l2 else 0
11
12            total = val1 + val2 + carry
13            carry = total // 10
14            curr.next = ListNode(total % 10)
15
16            curr = curr.next
17            l1 = l1.next if l1 else None
18            l2 = l2.next if l2 else None
19
20        return dummy.next
21
```

---
*Auto-documented on 2026-06-30 using [solution-tracker](https://github.com/chinthan59/Algo-diary)*
