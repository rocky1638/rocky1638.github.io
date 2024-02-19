---
created_at: 2022-11-12
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/balanced-binary-tree/
---

# 110. Balanced Binary Tree

```python
class Solution:
    def isBalanced(self, root: Optional[TreeNode]) -> bool:
        ans = True
        
        def recurse(node):
            nonlocal ans
            
            if node:
                lh = 1 + recurse(node.left)
                rh = 1 + recurse(node.right)
                
                if abs(lh-rh) > 1:
                    ans = False
                
                return max(lh, rh)
                
            else: return 0
                
        recurse(root)
        return ans
```

- [[dfs]] through the [[binary-tree]] and calculate the height of both the left subtree and the right subtree with [[recursion]].
	- have the recursive calls return their own height.
- if at any point the height of the left tree and right tree differ by more than 1, than our tree is not balanced.

Categories:: [[dfs]], [[binary-tree]], [[tree]], [[recursion]]
