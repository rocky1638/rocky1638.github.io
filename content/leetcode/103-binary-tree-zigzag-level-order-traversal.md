---
created_at: 2022-12-28
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/
---

# 103. Binary Tree Zigzag Level Order Traversal

```python
class Solution:
    def zigzagLevelOrder(self, root: Optional[TreeNode]) -> List[List[int]]:
        if not root:
            return []

        levels = []

        q = collections.deque([root])
        flip = False
        while q:
            level_len = len(q)
            if flip:
                levels.append([x.val for x in reversed(q)])
            else:
                levels.append([x.val for x in q])
            flip = not flip

            for _ in range(level_len):
                cur = q.popleft()
                if cur.left: q.append(cur.left)
                if cur.right: q.append(cur.right)
            
        return levels
```

- standard [[102-binary-tree-level-order-traversal]] with [[bfs]], but just append the level in reverse every other level.

Categories:: [[bfs]], [[binary-tree]], [[tree]]
