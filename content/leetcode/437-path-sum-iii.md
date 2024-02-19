# 437. Path Sum III

```python
class Solution:
    def pathSum(self, root: Optional[TreeNode], targetSum: int) -> int:
        """
        - at each recursion, we could either continue the path from the parent node,
          or start a new path at the current node.
        - collect all the possible sums down each full length path, starting from each node
        - at each node in the recursion, see how many subpaths in that path
          amounted to our targetSum
        """

        ans = 0
        def recurse(node, sums):
            nonlocal ans

            if node:
                sums = [x + node.val for x in sums]
                sums.append(node.val)

                for val in sums:
                    if val == targetSum:
                        ans += 1

                recurse(node.left, sums)
                recurse(node.right, sums)

                
        recurse(root, [])
        return ans
```

- along each branch of our [[recursion]] in the [[dfs]], we keep an [[array]] `sums` of the sums of all the possible subpaths if they had started on each of the previous nodes.
- similarly on each node, we check to see if any of the possible sums equal to our `targetSum`.

[[binary-tree]], [[tree]]