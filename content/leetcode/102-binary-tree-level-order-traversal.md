---
created_at: 2022-11-19
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/binary-tree-level-order-traversal/
---

# 102. Binary Tree Level Order Traversal

Given the `root` of a binary tree, return _the level order traversal of its nodes' values_. (i.e., from left to right, level by level).

```python
class Solution:
    def levelOrder(self, root: Optional[TreeNode]) -> List[List[int]]:
        if not root:
            return []
        
        levels = []
        
        q = deque([root])
        
        while q:
            len_level = len(q)
            levels.append([x.val for x in q])
            
            for _ in range(len_level):
                cur = q.popleft()
                if cur.left: q.append(cur.left)
                if cur.right: q.append(cur.right)
        return levels
```

- do a standard [[bfs]] while keeping track of levels.
- append the levels to a output [[array]].

Categories:: [[array]], [[bfs]], [[binary-tree]], [[tree]]
