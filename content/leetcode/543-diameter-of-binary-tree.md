---
created_at: 2022-11-15
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/diameter-of-binary-tree/
---

# 543. Diameter of Binary Tree

Given the `root` of a binary tree, return _the length of the **diameter** of the tree_.

The **diameter** of a binary tree is the **length** of the longest path between any two nodes in a tree. This path may or may not pass through the `root`.

The **length** of a path between two nodes is represented by the number of edges between them.

```python
# at each recursion, return the max height of the tree
class Solution:
    def diameterOfBinaryTree(self, root: Optional[TreeNode]) -> int:
        def recurse(node):
            nonlocal max_diameter
            if node:
                hl = recurse(node.left)
                hr = recurse(node.right)
                diameter = hl + hr

                max_diameter = max(max_diameter, diameter)
                return max(hl, hr) + 1
            
            return 0
        
        recurse(root)
        return max_diameter
```

- the max diameter centered at any node is equal to the sum of the max heights of the left and right subtrees.
- when we recurse, we return the max height of the subtree of the current node.

Categories:: [[binary-tree]], [[recursion]], [[dfs]]
