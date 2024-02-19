---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/validate-binary-search-tree/
---

# 98. Validate Binary Search Tree

```python
class Solution:
    def isValidBST(self, root: Optional[TreeNode]) -> bool:
        def recurse(node, low, hi):
            if not node:
                return True
            
            if node.val < hi and node.val > low:
                left_valid = recurse(node.left, low, node.val)
                right_valid = recurse(node.right, node.val, hi)
                return left_valid and right_valid
            
            else:
                return False
            
        return recurse(root, float("-inf"), float("inf"))
```

- we do a [[recursion]] through the [[binary-search-tree]], passing valid ranges for the subtree in the function call.

Categories:: [[recursion]], [[binary-tree]], [[tree]]
