---
created_at: 2023-01-07
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/reorder-list/
---

# 143. Reorder List

You are given the head of a singly linked-list. The list can be represented as:

$L_0$ → $L_1$ → … → $L_n-1$ → $L_n$

_Reorder the list to be on the following form:_

$L_0$ → $L_n$ → $L_1$ → $L_n - 1$ → $L_2$ → $L_n - 2$ → …

You may not modify the values in the list's nodes. Only nodes themselves may be changed.

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

    def reorderList(self, head: Optional[ListNode]) -> None:
        """
        Do not return anything, modify head in-place instead.
        """
        if not head: return None
        if not head.next: return head
        
        slow, fast = head, head

        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            
        # unlink the two lists
        cur = head
        while cur and cur.next != slow:
            cur = cur.next
        if cur: cur.next = None 

        # reverse the list that starts from where slow is now
        reversed_head = self.reverseList(slow)

        dummy = ListNode(0)
        cur = dummy
        while head or reversed_head:
            if head:
                cur.next = head
                cur = cur.next
                head = head.next
            if reversed_head:
                cur.next = reversed_head
                cur = cur.next
                reversed_head = reversed_head.next
        return dummy.next
```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[206-reverse-linked-list]].

## References.

Categories:: [[linked-list]]
