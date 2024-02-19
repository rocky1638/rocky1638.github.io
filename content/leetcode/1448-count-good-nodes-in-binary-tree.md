---
created_at: 2023-01-08
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/count-good-nodes-in-binary-tree/
---

# 1448. Count Good Nodes In Binary Tree

Given a binary tree `root`, a node _X_ in the tree is named **good** if in the path from root to _X_ there are no nodes with a value _greater than_ X.

Return the number of **good** nodes in the binary tree.

![](https://assets.leetcode.com/uploads/2020/04/02/test_sample_1.png)

```python
class Solution:
    def goodNodes(self, root: TreeNode) -> int:
        ans = 0

        def recurse(node, maxsofar):
            nonlocal ans
            
            if node:
                if node.val >= maxsofar:
                    ans += 1
                recurse(node.left, max(maxsofar, node.val))
                recurse(node.right, max(maxsofar, node.val))

        recurse(root, float("-inf"))
        return ans
```

- keep track of the maximum node value we’ve seen along the recursion path.
- a node is good if it is $\geq$ that maximum value.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[recursion]], [[tree]], [[binary-tree]]
