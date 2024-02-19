---
created_at: 2022-11-12
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/linked-list-cycle/
---

# 141. Linked List Cycle

```python
class Solution:
    def hasCycle(self, head: Optional[ListNode]) -> bool:
        slow, fast = head, head
        
        while slow and fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            
            if slow == fast:
                return True
            
        return False
```

- use the classic fast and slow pointer algorithm to find the cycle in a [[linked-list]].

Categories:: [[linked-list]], [[slow-fast-pointer]]
