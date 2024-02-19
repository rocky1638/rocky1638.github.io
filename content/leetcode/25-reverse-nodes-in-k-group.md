---
created_at: 2023-01-08
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/reverse-nodes-in-k-group/
---

# 25. Reverse Nodes In K-Group

Given the `head` of a linked list, reverse the nodes of the list `k` at a time, and return _the modified list_.

`k` is a positive integer and is less than or equal to the length of the linked list. If the number of nodes is not a multiple of `k` then left-out nodes, in the end, should remain as it is.
You may not alter the values in the list's nodes, only nodes themselves may be changed.


![](https://assets.leetcode.com/uploads/2020/10/03/reverse_ex1.jpg)

```python
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        prev, cur = None, head
        tail = head
        
        while cur:
            nex = cur.next
            cur.next = prev
            prev = cur
            cur = nex
        
        return prev, tail

    def reverseKGroup(self, head: Optional[ListNode], k: int) -> Optional[ListNode]:
        """
        - reverse the first k elements
        - return the head of the reversed list linked
          to the recursive of the rest of list
        """
        if not head:
            return None

        # find kth node
        cur = head
        # if k is 1, we want to end on the head node
        for _ in range(k-1):
            if cur:
                cur = cur.next
            else: break
        
        rest = None
        # store rest of list's head
        if cur:
            rest = cur.next

            # disconnect rest of list
            cur.next = None

            # reverse the list
            reversed_head, reversed_tail = self.reverseList(head)

            # link tail to rest of list
            reversed_tail.next = self.reverseKGroup(rest, k)
            
            return reversed_head

        else:
            return head
```

- we reverse the first `k` nodes if they exist, and then connect the tail of this reversed list to the result of the recursive call on the rest of the list.
	- because of the recursion, we return the head of the entire list at the end of the recursive function.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[206-reverse-linked-list]]

## References.

Categories:: [[linked-list]], [[recursion]]
