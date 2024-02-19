# 328. Odd Even Linked List

```python
class Solution:
   def oddEvenList(self, head):
    odds = ListNode(0)
    evens = ListNode(0)
    oddsHead = odds
    evensHead = evens
    isOdd = True
    while head:
        if isOdd:
            odds.next = head
            odds = odds.next
        else:
            evens.next = head
            evens = evens.next
        isOdd = not isOdd
        head = head.next
    evens.next = None
    odds.next = evensHead.next
    return oddsHead.next 
```

- keep an even and odd [[linked-list]].
- alternate our `isOdd` counter, and add to either the odd or even linked list.
- at the end, set the `next` pointer of even list to be `None`, and the next pointer of the odd linked list to be the head of the even linked list.
