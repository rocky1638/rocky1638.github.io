---
created_at: 2022-12-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/swap-nodes-in-pairs/
---

# 24. Swap Nodes in Pairs

```python
class Solution:
    def swapPairs(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if not head:
            return None
        if not head.next:
            return head

        dummy = ListNode(-1) 
        dummy.next = head

        # initialize the pointers on the nodes before the 
        # first ones that we need to swap
        left, right = dummy, head

        while left and left.next and right and right.next:
            right_of_right = right.next.next
            toswap_left = left.next
            toswap_right = right.next

            left.next = toswap_right
            toswap_right.next = toswap_left
            toswap_left.next = right_of_right

			# these swaps are not intuitive, just draw it out
            left = toswap_left
            right = right_of_right
        return dummy.next
```

- create a dummy node for ease of coding.
- have pointers at the nodes before the ones we want to swap.
- perform the swap.
- update the pointers.

Categories:: [[linked-list]], [[two-pointers]]
