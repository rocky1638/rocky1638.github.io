---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/binary-tree-right-side-view/
---

# 199. Binary Tree Right Side View

Given the `root` of a binary tree, imagine yourself standing on the **right side** of it, return _the values of the nodes you can see ordered from top to bottom_.

![](https://assets.leetcode.com/uploads/2021/02/14/tree.jpg)

```python
class Solution:
    def rightSideView(self, root: Optional[TreeNode]) -> List[int]:
        if not root:
            return []
        
        ans = [root.val]
        
        q = deque([root])
        
        while q:
            level_len = len(q)
            
            for _ in range(level_len):
                cur = q.popleft()
                if cur.left: q.append(cur.left)
                if cur.right: q.append(cur.right)
            if q:
                ans.append(q[-1].val)
        return ans
```

- do a level-order traversal just like [[102-binary-tree-level-order-traversal]] and just append the right value in each level to `ans`.

Categories:: [[tree]], [[binary-tree]], [[bfs]]
