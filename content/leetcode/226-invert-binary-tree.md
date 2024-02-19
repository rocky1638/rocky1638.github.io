---
created_at: 2022-11-11
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/invert-binary-tree/
---

# 226. Invert Binary Tree

Given the `root` of a binary tree, invert the tree, and return _its root_.

![](https://assets.leetcode.com/uploads/2021/03/14/invert1-tree.jpg)

```python
class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        def recurse(node):
            if node:
                node.left, node.right = node.right, node.left
                recurse(node.left)
                recurse(node.right)
        
        recurse(root)
        return(root)
```

- recurse down the tree and swap at every node.
- tree is guaranteed to be well-formed.

Categories:: [[recursion]], [[binary-tree]], [[tree]]
