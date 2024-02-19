---
created_at: 2023-01-25
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/populating-next-right-pointers-in-each-node/
---

# 116. Populating Next Right Pointers In Each Node

You are given a **perfect binary tree** where all leaves are on the same level, and every parent has two children. The binary tree has the following definition:

![](https://assets.leetcode.com/uploads/2019/02/14/116_sample.png)

```python
class Solution:
    def connect(self, root: 'Optional[Node]') -> 'Optional[Node]':
        if root:
            if root.right:
                if root.next:
                    root.right.next = root.next.left
                self.connect(root.right)
            
            if root.left:
                root.left.next = root.right
                self.connect(root.left)
        
        return root
```

- recursively populate the next pointers of the current node’s children.
- after populating, recurse on the children *(after their `next` pointers have been set)*.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[117-populating-next-right-pointers-in-each-node-ii]].

## References.

Categories:: [[recursion]], [[binary-tree]], [[tree]]
