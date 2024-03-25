---
title: 23. merge k sorted lists
type: leetcode
aliases: 
difficulty: 🔴
link: https://leetcode.com/problems/merge-k-sorted-lists/
date: 2022-11-25
updated: 2024-03-20
tags:
  - heap
  - linked-list
  - hashmap
---

You are given an array of `k` linked-lists `lists`, each linked-list is sorted in ascending order.

_Merge all the linked-lists into one sorted linked-list and return it._

## solution

We use a heap to keep track of the next value that we need to append to our output linked list.
Then, use a hashmap to keep track of actual node addresses based on each list, because we can’t put the actual node objects into our heap.

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

Alternatively, we can also use a list to store the addresses of the actual nodes.

```python
def mergeKLists(self, lists: List[Optional[ListNode]]) -> Optional[ListNode]:
	dummy = ListNode()
	# heap[i] = [node.val, index of list that the node is in]
	cur_pointers = []
	minheap = []
	  
	# add all first values to heap
	# add all pointers to array
	for i, l in enumerate(lists):
		if l:
			heappush(minheap, (l.val, i))
		cur_pointers.append(l)
	  
	curnode = dummy
	while minheap:
		next_val, list_idx = heappop(minheap)
		  
		# add value to output list
		curnode.next = cur_pointers[list_idx]
		curnode = curnode.next
		  
		# add next value in the list onto heap if it exists
		cur_pointers[list_idx] = cur_pointers[list_idx].next
		if cur_pointers[list_idx] is not None:
			heappush(minheap, (cur_pointers[list_idx].val, list_idx))

	return dummy.next
```
