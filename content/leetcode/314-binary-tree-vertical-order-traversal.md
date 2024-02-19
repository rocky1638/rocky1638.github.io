# 314. Binary Tree Vertical Order Traversal

```python
class Solution:
    def verticalOrder(self, root: Optional[TreeNode]) -> List[List[int]]:
        if not root:
            return None
        
        # root is at column 0, left child -1, right child +1
        columns = defaultdict(list)
        ans = []
        
        # q[i] = (node, column_idx)
        q = deque([(root, 0)])
        
        # level order traversal with bfs
        while q:
            cur, col = q.popleft()
            columns[col].append(cur.val)
            
            if cur.left: q.append((cur.left, col-1))
            if cur.right: q.append((cur.right, col+1))
        
        for key in sorted(list(columns.keys())):
            ans.append(columns[key])
        return ans
            
```

- keep a [[hashmap]] that tracks the vertical columns of nodes.
- keep track of column index as we [[bfs]], where the root node has a column of 0.

[[binary-tree]], [[tree]]