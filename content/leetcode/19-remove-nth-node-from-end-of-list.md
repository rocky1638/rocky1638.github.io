---
created_at: 2022-12-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/remove-nth-node-from-end-of-list/
---

# 19. Remove Nth Node from End of List

```python
class Solution:
    def removeNthFromEnd(self, head: Optional[ListNode], n: int) -> Optional[ListNode]:
        fast, slow = head, head 

        # move fast pointer ahead
        for _ in range(n):
           fast = fast.next

        if fast is None: # then n == len(list)
            # remove the root node (just return the next node)
            return slow.next
        else:
            while fast.next:
                # advance both pointers in lockstep
                slow = slow.next
                fast = fast.next
            n = slow.next.next
            slow.next = n
            return head
```

- we use a [[slow-fast-pointer]], a variation of the general [[two-pointers]] strategy to be able to remove the nth last node in only one pass.
- move the fast pointer ahead by `n` spaces, so that we can then move both pointers together, and once `fast` reaches the end, `slow` will be on the pointer before the one we want to remove.
- there’s an edge case in which `n` equals the length of the [[linked-list]], meaning we need to remove the `head` node.
	- in this case, after moving our fast pointer separately, it will be past the end of the list and equal `None`.
	- in this case, just return `head.next`, essentially removing the first node.

Categories:: [[slow-fast-pointer]], [[two-pointers]], [[linked-list]]
