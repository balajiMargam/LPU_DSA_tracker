# Linked List Cycle Detection

- Link - https://neetcode.io/problems/linked-list-cycle-detection/question

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next

class Solution:
    def hasCycle(self, head: Optional[ListNode]) -> bool:
        seen = set()
        x = head
        while x:
            if x in seen:
                return True
            seen.add(x)
            x = x.next
        return False
```