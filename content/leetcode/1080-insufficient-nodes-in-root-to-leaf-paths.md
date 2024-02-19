---
created_at: 2023-01-25
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/insufficient-nodes-in-root-to-leaf-paths/
---

# 1080. Insufficient Nodes In Root To Leaf Paths

Given the `root` of a binary tree and an integer `limit`, delete all **insufficient nodes** in the tree simultaneously, and return _the root of the resulting binary tree_.

A node is **insufficient** if every root to **leaf** path intersecting this node has a sum strictly less than `limit`.

A **leaf** is a node with no children.

```python
class Solution:
    def sufficientSubset(self, root: Optional[TreeNode], limit: int) -> Optional[TreeNode]:
	    # a leaf is invalid if the path that has lead to it + it's value
	    # is less than limit.
        if root.left == root.right:
            return None if root.val < limit else root

		# if we reach a leaf that is an insufficient path, then the ancestor
		# nodes of the leaf will also be insufficient because the path sum
		# can't add up to limit either.
        if root.left:
            root.left = self.sufficientSubset(root.left, limit-root.val)
        if root.right:
            root.right = self.sufficientSubset(root.right, limit-root.val)
        
        return root if root.left or root.right else None
```

- we decrement `limit` in our recursive calls.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[recursion]], [[tree]]
