---
created: 2022-11-30
type: leetcode
difficulty: 🟢
link: https://leetcode.com/problems/add-two-numbers/
---

# 2. Add Two Numbers

```python
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        ret = ListNode()
        cur = ret
        carry = 0
        
        while l1 or l2:
            # add at position
            subsum = 0
            if l1: subsum += l1.val
            if l2: subsum += l2.val
            subsum += carry
            
            # create output node
            new_node = ListNode(subsum % 10)
            cur.next = new_node
            cur = cur.next
            
            # update carry
            carry = 1 if subsum > 9 else 0
            
            # move pointers
            l1 = l1.next if l1 else None
            l2 = l2.next if l2 else None
            
        if carry:
            cur.next = ListNode(1)
            
        return ret.next
```

- because the two [[linked-list|linked-lists]] are reversed, we just use grade school addition formula with a `carry` variable to do the addition.
- use a dummy node for ease of coding.

Categories:: [[math]], [[linked-list]]
