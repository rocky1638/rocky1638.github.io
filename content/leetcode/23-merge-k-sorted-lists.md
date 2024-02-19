---
created_at: 2022-11-25
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/merge-k-sorted-lists/
---

# 23. Merge k Sorted Lists

```python
class Solution:
    def mergeKLists(self, lists: List[Optional[ListNode]]) -> Optional[ListNode]:
        if not lists:
            return None
        
        dummy = ListNode(-1)
        cur = dummy
        heap = []
        # idx of list in lists -> node object of current pointer in list
        list_pointers = defaultdict()
        
        for i, node in enumerate(lists):
            if node:
                heap.append((node.val, i))
                list_pointers[i] = node
            
        heapq.heapify(heap)
        
        while heap:
            # pop from heap and get node
            val, list_idx = heapq.heappop(heap)
            node = list_pointers[list_idx]
            
            # append to result and advance cur pointer
            cur.next = node
            cur = cur.next
            
            # find next node to put in heap from this list
            next_node = node.next
            
            list_pointers[list_idx] = next_node
            
            if next_node:
                heapq.heappush(heap, (next_node.val, list_idx))
        
        return dummy.next
```

- we use a [[heap]] to keep track of the next value that we need to append to our output [[linked-list]].
- use a [[hashmap]] to keep track of actual node addresses based on each list, because we can’t put the actual node objects into our [[heap]].

Categories:: [[heap]], [[linked-list]], [[hashmap]]
