---
created_at: 2022-12-12
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/same-tree/
---

# 100. Same Tree

```python
class Solution:
    def isSameTree(self, p: Optional[TreeNode], q: Optional[TreeNode]) -> bool:
        if p is None and q is None: return True
        if p is None or q is None: return False

        if p.val != q.val:
            return False
        
        return self.isSameTree(p.left, q.left) and self.isSameTree(p.right, q.right)
```

- basic [[dfs]] using [[recursion]] with both of the [[binary-tree]].

Categories:: [[binary-tree]], [[tree]], [[recursion]], [[dfs]]
