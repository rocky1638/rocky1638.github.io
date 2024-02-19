---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/
---

# 105. Construct Binary Tree from Preorder and Inorder Traversal

Given two integer arrays `preorder` and `inorder` where `preorder` is the preorder traversal of a binary tree and `inorder` is the inorder traversal of the same tree, construct and return _the binary tree_.

```python
class Solution:
    def buildTree(self, preorder: List[int], inorder: List[int]) -> Optional[TreeNode]:
        preorderIdx = 0
        inorderMap = defaultdict()
        
        def recurse(inorderL, inorderR):
            nonlocal preorderIdx
            
            if inorderL > inorderR:
                return
            
            root = TreeNode(preorder[preorderIdx])
            
            preorderIdx += 1
            
            root.left = recurse(inorderL, inorderMap[root.val]-1)
            root.right = recurse(inorderMap[root.val]+1, inorderR)
            
            return root
        
        for i, val in enumerate(inorder):
            inorderMap[val] = i
        
        return recurse(0, len(inorder)-1)
```

- note that the preorder traversal is created by recursing using the order of `root, left, right`.
- the `inorder` traversal is distributed the same as the original tree when we scan the tree from left to right.
	- for any node in the `inorder`, all the left subtree nodes are on the left of it, and all the right subtree nodes are on the right of it.
- the key insight is that we should recursively construct the tree in the same order that the `preorder` traversal goes in, so that the next root node we need to consider is always the next node in the `preorder` array!
	- then, we just use the `inorder` array for additional data, and to narrow down our search radius.
- we keep a [[hashmap]] of the index that each value is at in the `inorder` array for $O(1)$ lookup in the recursive calls.

Categories:: [[binary-tree]], [[tree]], [[recursion]], [[array]], [[hashmap]]
