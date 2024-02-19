# 285. Inorder Successor in BST

```python
class Solution:
    def inorderSuccessor(self, root: TreeNode, p: TreeNode) -> Optional[TreeNode]:
        # inorder is left, root, right
        ans = None
        found_p = False
        def inorder(node):
            nonlocal ans
            nonlocal found_p

            if node:
                inorder(node.left)
                # do something with root
                if found_p and ans is None:
                    ans = node
                    return

                if node == p:
                    found_p = True
                inorder(node.right)
        inorder(root)
        return ans
```

- we do an in-order traversal of the [[binary-tree]], and once we see the target node `p`, we flip a flag, and set our `ans` to the next node that we see in the traversal.

[[dfs]]