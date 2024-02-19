# 234. Palindrome Linked List

```python
class Solution:
    def isPalindrome(self, head: Optional[ListNode]) -> bool:
        n = 0

        def reverse(node):
            prev = None

            while node:
                n = node.next
                node.next = prev
                prev, node = node, n
            return prev

        # find length of list
        cur = head
        while cur:
            n += 1
            cur = cur.next
        
        # move to center of list and reverse second half
        cur = head
        for _ in range(n // 2):
            cur = cur.next
        reversed_head = reverse(cur)

        for _ in range(n // 2):
            if head.val != reversed_head.val:
                return False
            head = head.next
            reversed_head = reversed_head.next

        return True
```

- we find the middle of the [[linked-list]], and reverse the second half of the linked list ([[206-reverse-linked-list]]).
- then, using [[two-pointers]] from either end, return `False` if we see a mismatched pair, or return `True` if every pair matches.