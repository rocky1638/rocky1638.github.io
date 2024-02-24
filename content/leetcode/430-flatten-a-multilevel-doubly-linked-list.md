---
date: 2022-11-17
title: 430. flatten a multilevel doubly linked list
tags:
  - linked-list
  - dfs
updated: 2024-02-24
---

You are given a doubly linked list, which contains nodes that have a next pointer, a previous pointer, and an additional **child pointer**. This child pointer may or may not point to a separate doubly linked list, also containing these special nodes. These child lists may have one or more children of their own, and so on, to produce a **multilevel data structure** as shown in the example below.

Given the `head` of the first level of the list, **flatten** the list so that all the nodes appear in a single-level, doubly linked list. Let `curr` be a node with a child list. The nodes in the child list should appear **after** `curr` and **before** `curr.next` in the flattened list.


![](https://assets.leetcode.com/uploads/2021/11/09/flatten11.jpg)

## solution

```python
class Solution:
	def flatten(self, head: 'Optional[Node]') -> 'Optional[Node]':
		def recurse(node):
			if not node:
				return None
				# base case, nowhere to recurse so just return the node
			elif not node.next and not node.child:
				return node
			else:
				n = node.next
				# we'll return when we reach a basecase node, so that'll be the
				# tail that we connect between our current node and the next node
				if node.child:
					tail = recurse(node.child)

					node.next = node.child
					node.child.prev = node
					node.child = None
					tail.next = n
					
					if n:
						n.prev = tail
					else:
						# we want to return tail instead of recursing on node.next
						# if node.next is None (if we're at the end of the level)
						# (similar idea to the above elif case, because 
						# tail is guaranteed to have no next or child)
						
						# tail is the end of the flattened list that
						# was processed in the recursive call
						return tail
				*return* recurse(n)

		recurse(head)
		return head
```
