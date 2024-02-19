# 445. Add Two Numbers II

## Trivial.

```python
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        a = 0
        b = 0
        
        while l1:
            a *= 10
            a += l1.val
            l1 = l1.next
        
        while l2:
            b *= 10
            b += l2.val
            l2 = l2.next
            
        c = a + b
        
        dummy = ListNode()
        cur = dummy
        for digit in str(c):
            new_node = ListNode(int(digit))
            cur.next = new_node
            cur = new_node
        
        return dummy.next
```

- read the two numbers, add them, and make a new linked list.

## Reverse linked lists and add.

```python
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        def reverseList(head):
            prev, cur = None, head

            while cur:
                nex = cur.next
                cur.next = prev
                prev = cur
                cur = nex

            return prev
        
        def addTwoLists(l1, l2):
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
        
        l1 = reverseList(l1)
        l2 = reverseList(l2)
        
        sum_reversed = addTwoLists(l1, l2)
        return reverseList(sum_reversed)
        
        
```

- reverse both lists ([[206-reverse-linked-list]]), and then this question becomes [[2-add-two-numbers]].
- we literally just use those two problems to solve this problem.

[[linked-list]], [[math]]