---
title: 430. flatten a multilevel doubly linked list
tags:
  - linked-list
  - recursion
  - dfs
---

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
						return tail
				return recurse(n)

		recurse(head)
		return head
```

![](https://assets.leetcode.com/uploads/2021/11/09/flatten11.jpg)
