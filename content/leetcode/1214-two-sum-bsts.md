---
created_at: 2023-01-19
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/two-sum-bsts/
---

# 1214. Two Sum BSTs

Given the roots of two binary search trees, `root1` and `root2`, return `true` if and only if there is a node in the first tree and a node in the second tree whose values sum up to a given integer `target`.

## Recursion with memoization.

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def twoSumBSTs(self, root1: Optional[TreeNode], root2: Optional[TreeNode], target: int) -> bool:
        """
        - recurse on both trees in parallel.
        - binary search.
        """
        memo = {}
        def recurse(n1, n2):
            if n1 and n2:
                if (id(n1), id(n2)) in memo:
                    return memo[(id(n1), id(n2))]
                cursum = n1.val + n2.val
                if cursum == target:
                    return True

                if cursum < target:
                    memo[(id(n1), id(n2))] = recurse(n1.right, n2) or recurse(n1, n2.right)
                else:
                    memo[(id(n1), id(n2))] = recurse(n1.left, n2) or recurse(n1, n2.left)
                
                return memo[(id(n1), id(n2))]
            return False
            
        return recurse(root1, root2)
```

- recursive approach with memoization.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[1-two-sum]].

## References.

Categories:: [[tree]], [[binary-search-tree]], [[recursion]], [[memoization]]
