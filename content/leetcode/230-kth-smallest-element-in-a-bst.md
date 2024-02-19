# 230. Kth Smallest Element in a BST

```python
class Solution:
    def kthSmallest(self, root: Optional[TreeNode], k: int) -> int:
        # left, node, right traversal gives u values in order?
        count = 0
        ans = None
        
        def dfs(node):
            nonlocal count
            nonlocal ans
            
            if node:
                dfs(node.left)
                count += 1
                if count == k:
                    ans = node.val
                    return
                dfs(node.right)
                
        dfs(root)
        return ans
```

- the property of a [[binary-search-tree]] is that an in-order traversal yields the values in arithmetic order.
- so, if we just do an in-order traversal and keep track of which step we are in the traversal, we can just return the value of kth value that we see.

[[dfs]], [[recursion]], [[tree]], [[binary-tree]]