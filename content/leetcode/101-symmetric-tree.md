---
created_at: 2022-12-27
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/symmetric-tree/
---

# 101. Symmetric Tree

```python
class Solution:
    def isSymmetric(self, root: Optional[TreeNode]) -> bool:
        if not root:
            return True

        def recurse(ln, rn):
            if not ln and not rn: return True
            if ln and rn:
                if ln.val == rn.val:
                    return recurse(ln.left, rn.right) and recurse(rn.left, ln.right)
            # if one of them is None, or values are not equal
            return False
        
        return recurse(root.left, root.right)
```

- we do a [[recursion]] on the [[binary-tree]] with two nodes in the arguments.
- start with recursing on the left and right subtrees, because it doesn’t matter what the value of `root` is.

Categories:: [[binary-tree]], [[tree]], [[recursion]]
