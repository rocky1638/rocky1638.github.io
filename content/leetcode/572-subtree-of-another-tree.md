---
created_at: 2023-01-08
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/subtree-of-another-tree/
---

# 572. Subtree Of Another Tree

Given the roots of two binary trees `root` and `subRoot`, return `true` if there is a subtree of `root` with the same structure and node values of `subRoot` and `false` otherwise.

A subtree of a binary tree `tree` is a tree that consists of a node in `tree` and all of this node's descendants. The tree `tree` could also be considered as a subtree of itself.

![](https://assets.leetcode.com/uploads/2021/04/28/subtree1-tree.jpg)

```python
class Solution:
    def isSameTree(self, p: Optional[TreeNode], q: Optional[TreeNode]) -> bool:
        if p is None and q is None: return True
        if p is None or q is None: return False

        if p.val != q.val:
            return False
        
        return self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)

    def isSubtree(self, root: Optional[TreeNode], subRoot: Optional[TreeNode]) -> bool:
        # base cases
        if root is None and subRoot is None:
            return True
        if root is None or subRoot is None:
            return False

        if root.val == subRoot.val:
            if self.isSameTree(root, subRoot):
                return True
        return self.isSubtree(root.left, subRoot) or self.isSubtree(root.right, subRoot)
```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[100-same-tree]].

## References.

Categories:: [[tree]], [[binary-tree]], [[recursion]]
