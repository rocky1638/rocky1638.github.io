---
created_at: 2022-11-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/
---

# 236. Lowest Common Ancestor of a Binary Tree

Given a binary tree, find the lowest common ancestor (LCA) of two given nodes in the tree.

According to the [definition of LCA on Wikipedia](https://en.wikipedia.org/wiki/Lowest_common_ancestor): “The lowest common ancestor is defined between two nodes `p` and `q` as the lowest node in `T` that has both `p` and `q` as descendants (where we allow **a node to be a descendant of itself**).”

```python
class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        ans = None
        
        def recurse(node):
            nonlocal ans

			if ans:
				return # stop early
            
            if node:
                has_p, has_q = False, False
                if node == p:
                    has_p = True
                if node == q:
                    has_q = True

                l_has_p, l_has_q = recurse(node.left)
                r_has_p, r_has_q = recurse(node.right)
                
                has_p = has_p or l_has_p or r_has_p
                has_q = has_q or l_has_q or r_has_q
            
                if has_p and has_q and ans == None:
                    ans = node
                return has_p, has_q
            return False, False
                
        recurse(root)
        return ans
```

- at each step in the [[recursion]] through the [[binary-tree]], we will return whether the current node has `p` and `q` as descendants.
	- we do this by first recursing on the children of the current node.
- because we recurse on the children first, the first node that we reach that satisfies `has_q` and `has_p` must be the lowest common ancestor.

Categories:: [[dfs]], [[recursion]], [[binary-tree]], [[tree]]
