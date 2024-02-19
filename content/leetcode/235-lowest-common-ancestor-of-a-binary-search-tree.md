---
created_at: 2022-11-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/
---

# 235. Lowest Common Ancestor of a Binary Search Tree

Given a binary search tree (BST), find the lowest common ancestor (LCA) node of two given nodes in the BST.

According to the [definition of LCA on Wikipedia](https://en.wikipedia.org/wiki/Lowest_common_ancestor): “The lowest common ancestor is defined between two nodes `p` and `q` as the lowest node in `T` that has both `p` and `q` as descendants (where we allow **a node to be a descendant of itself**).”

```python
class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        ans = None
        hi, low = max(p.val, q.val), min(p.val, q.val)
        
        def recurse(node):
            if node.val > hi:
                return recurse(node.left)
            elif node.val < low:
                return recurse(node.right)
            else:
                return node
        
        return recurse(root)
```

- because a [[binary-search-tree]] has the property of every left child being smaller and right child being larger, we know that if we find a node that’s valued `lo <= node.val <= hi`, we are guaranteed to have found the lowest common ancestor.
![[235-e1.excalidraw]]
- the lowest common ancestor can’t possibly be the child of one of these nodes because one of either `hi` or `low` will be out of the possible range of the child node’s children.

Categories:: [[recursion]], [[binary-search-tree]], [[tree]]
