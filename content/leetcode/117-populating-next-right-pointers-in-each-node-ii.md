---
created_at: 2022-12-06
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/populating-next-right-pointers-in-each-node-ii/
---

# 117. Populating Next Right Pointers in Each Node II

## Level-order traversal using a [[queue]].

```python
class Solution:
    def connect(self, root: 'Node') -> 'Node':
        if not root:
            return root

        q = collections.deque([root])

        # level-order traversal of the binary tree
        while q:
            # iterate through level, set right pointers
            for i in range(len(q)):
                if i+1 < len(q):
                    print(q[i].val, q[i+1].val)
                    q[i].next = q[i+1]

            level_len = len(q)

            for _ in range(level_len):
                curnode = q.popleft()
                if curnode.left: q.append(curnode.left)
                if curnode.right: q.append(curnode.right)
        return root
```

- do a level-order traversal on the [[binary-tree]] using [[bfs]] and once we complete each level, just go through the array and link the `next` pointers.

## Recursive.

```python
"""
Treat each level as a linked list, and assemble the next pointers
for the level below while iterating through the current level.
"""
class Solution:
    
    def find_next_for_child(self, node):
        curr = node.next
        
        while curr:
            if curr.left:
                return curr.left
            if curr.right:
                return curr.right
            curr = curr.next
            
        return None    
            
    
    def connect(self, root: 'Node') -> 'Node':
        if root:
            if root.right:      
                root.right.next = self.find_next_for_child(root)
                self.connect(root.right)
            if root.left:
                if root.right:
                    root.left.next = root.right
                else:    
                    root.left.next = self.find_next_for_child(root)
                self.connect(root.left)
                
        return root
```

- find the next node for your children nodes by looking at the `next` node in the parent’s row.
- only move onto the lower level once it is all connected with `next` pointers.

![[117-e1.excalidraw|1000]]

Categories:: [[binary-tree]], [[tree]], [[dfs]], [[bfs]], [[recursion]]
