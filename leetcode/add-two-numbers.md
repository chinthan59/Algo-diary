# [Add Two Numbers](https://leetcode.com/problems/add-two-numbers/submissions/2051651581/)

---

## Approach: Two Pointers

The solution utilizes a two-pointer technique to traverse both linked lists simultaneously, adding corresponding node values and handling carry-over. It maintains a dummy node to simplify the code and avoid edge cases. The core insight is to process the lists from left to right, keeping track of the carry for the next iteration.

## Algorithm Steps
1. Create a dummy node to simplify the code and avoid edge cases
2. Initialize two pointers, one for each linked list, and a carry variable
3. Traverse both linked lists, adding corresponding node values and handling carry-over
4. Create a new node with the sum modulo 10 and update the carry for the next iteration
5. Move the pointers to the next nodes in both linked lists

## Complexity
- **Time**: O(max(m, n)) where m and n are the lengths of the input linked lists, because we process each node exactly once
- **Space**: O(max(m, n)) as we create a new linked list with a maximum length of max(m, n) + 1 (in case of a carry-over)

## Patterns Used
`two pointers` `linked list traversal` `dummy node`

## Edge Cases
- Handling lists of different lengths
- Handling cases where the sum of two nodes' values exceeds 9, resulting in a carry-over
- Returning the next node of the dummy node to exclude the dummy node itself

## Alternative Approaches
- Using recursion instead of iteration to traverse the linked lists
- Using a stack to store the nodes and then reversing the result

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
