---
created_at: 2022-11-11
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/merge-two-sorted-lists/
---

# 21. Merge Two Sorted Lists

```python
class Solution:
    def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
        dummy = ListNode()
        cur = dummy
        
        while list1 or list2:
            if list1 and list2:
                if list1.val < list2.val:
                    cur.next = ListNode(list1.val)
                    list1 = list1.next
                else:
                    cur.next = ListNode(list2.val)
                    list2 = list2.next
            elif list1:
                cur.next = ListNode(list1.val)
                list1 = list1.next
            else:
                cur.next = ListNode(list2.val)
                list2 = list2.next
            cur = cur.next
        
        return dummy.next
```

- iterate through both [[linked-list]] and just pick the smaller value each time.
- use a dummy node to make pointer logic more simple.

Categories:: [[linked-list]]
