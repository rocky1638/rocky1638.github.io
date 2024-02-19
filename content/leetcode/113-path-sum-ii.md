---
created_at: 2022-12-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/path-sum-ii/
---

# 113. Path Sum II

```python
class Solution:
    def pathSum(self, root: Optional[TreeNode], targetSum: int) -> List[List[int]]:
        if not root:
            return []

        ans = []
        acc = [root.val]
        tally = root.val

        def recurse(node):
            nonlocal ans
            nonlocal tally
            
            if not node.left and not node.right:
                if tally == targetSum:
                    ans.append(acc[:])
            else:
                if node.left:
                    acc.append(node.left.val)
                    tally += node.left.val
                    recurse(node.left)
                    tally -= node.left.val
                    acc.pop()
                if node.right:
                    acc.append(node.right.val)
                    tally += node.right.val
                    recurse(node.right)
                    tally -= node.right.val
                    acc.pop()

        recurse(root)
		return ans
```

- simple [[dfs]] with [[recursion]] on the [[binary-tree]].
- keep an accumulator [[array]], if we reach a leaf and have the correct path sum, add it to the output array.

Categories:: [[dfs]], [[recursion]], [[binary-tree]], [[tree]], [[array]]
