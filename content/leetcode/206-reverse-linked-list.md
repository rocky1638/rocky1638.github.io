---
created_at: 2022-11-13
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/reverse-linked-list/
---

# 206. Reverse Linked List

```python
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        prev, cur = None, head
        
        while cur:
            nex = cur.next
            cur.next = prev
            prev = cur
            cur = nex
        
        return prev
```

- use two pointers, starting `prev` before the start of the [[linked-list]] and `cur` at the first node.
- temporarily store the next node in a variable, flip the arrow, and then move the two pointers further along the list.

Categories:: [[linked-list]], [[two-pointers]]
