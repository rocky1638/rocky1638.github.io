---
created_at: 2022-12-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/sort-list/
---

# 148. Sort List

```python
class Solution:
    def sortList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        def mergesort(left, numnodes):
            if numnodes == 0: return None
            if numnodes == 1:
                left.next = None
                return left
            if numnodes == 2:
                # sort the two nodes
                right = left.next
                if left.val > right.val:
                    right.next = left
                    left.next = None
                    return right
                else:
                    right.next = None
                    return left

            right = left
            rnumnodes = numnodes
            for _ in range(numnodes // 2):
                right = right.next
                rnumnodes -= 1
            
            # recursively sort left and right half
            lhead = mergesort(left, numnodes // 2)
            rhead = mergesort(right, rnumnodes)

            # merge the two lists
            dummy = ListNode(0)
            cur = dummy
            while lhead or rhead:
                if lhead and rhead:
                    if lhead.val > rhead.val:
                        cur.next = rhead
                        rhead = rhead.next
                    else:
                        cur.next = lhead
                        lhead = lhead.next
                elif lhead:
                    cur.next = lhead
                    lhead = lhead.next
                else:
                    cur.next = rhead
                    rhead = rhead.next
                cur = cur.next
            return dummy.next

        # find length of linked list
        cur = head
        n = 0
        while cur:
            n += 1
            cur = cur.next
 
        return mergesort(head, n)
```

- standard recursive implementation of merge sort on the [[linked-list]].
- [[divide-and-conquer]] all the way down until we reach our base cases of lengths 0, 1, and 2.
	- sort these small pieces and then merge the two halves together again.

Categories:: [[recursion]], [[sorting]], [[divide-and-conquer]], [[linked-list]]
