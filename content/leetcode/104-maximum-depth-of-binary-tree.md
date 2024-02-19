---
created_at: 2022-11-15
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/maximum-depth-of-binary-tree/
---

# 104. Maximum Depth of Binary Tree

Given the `root` of a binary tree, return _its maximum depth_.

A binary tree's **maximum depth** is the number of nodes along the longest path from the root node down to the farthest leaf node.

![](https://assets.leetcode.com/uploads/2020/11/26/tmp-tree.jpg)

```python
class Solution:
    def maxDepth(self, root: Optional[TreeNode]) -> int:
        def recurse(node):
            if node:
                return 1 + max(recurse(node.left), recurse(node.right))
            return 0
            
        return recurse(root)
```

- we use [[recursion]] on the [[binary-tree]].
- at each node, we return 1 plus the maximum height of the left and right subtrees.

Categories:: [[binary-tree]], [[tree]], [[recursion]]
