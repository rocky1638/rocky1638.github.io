---
created_at: 2023-01-27
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/insert-into-a-binary-search-tree/
---

# 701. Insert Into A Binary Search Tree

You are given the `root` node of a binary search tree (BST) and a `value` to insert into the tree. Return _the root node of the BST after the insertion_. It is **guaranteed** that the new value does not exist in the original BST.

**Notice** that there may exist multiple valid ways for the insertion, as long as the tree remains a BST after insertion. You can return **any of them**.

```python
class Solution:
    def insertIntoBST(self, root: Optional[TreeNode], val: int) -> Optional[TreeNode]:
        def recurse(node):
            if node is None:
                return TreeNode(val)
            
            if node.val < val:
                node.right = recurse(node.right)
                return node
            else:
                node.left = recurse(node.left)
                return node
                
        return recurse(root)
```

- basic recursion, just remember that the new value is always inserted as a leaf.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[binary-search-tree]], [[tree]], [[recursion]]
