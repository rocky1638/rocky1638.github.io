# 662. Maximum Width of Binary Tree

```python
class Solution:
    def widthOfBinaryTree(self, root: Optional[TreeNode]) -> int:
        if not root: return 0

        ans = 0
        q = collections.deque([(root, 1)])

        while q:
            level_len = len(q)
            ans = max(ans, q[-1][1]-q[0][1]+1)

            for _ in range(level_len):
                curnode, idx = q.popleft()
                if curnode.left: q.append((curnode.left, idx*2))
                if curnode.right: q.append((curnode.right, idx*2+1))
            
        return ans
```

- we use [[bfs]] through the [[binary-tree]] to do a [[102-binary-tree-level-order-traversal]].
	- for every level, we also index each node as if it were part of a full binary tree.
	- we do this by making each left child have index $2i$ and each right child have index $2i+1$.
	- then, the difference of the indexes of the leftmost and rightmost node on each level give us the width of the level.

[[tree]]