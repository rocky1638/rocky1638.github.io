---
created_at: 2022-12-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/graph-valid-tree/
---

# 261. Graph Valid Tree

You have a graph of `n` nodes labeled from `0` to `n - 1`. You are given an integer n and a list of `edges` where `edges[i] = [ai, bi]` indicates that there is an undirected edge between nodes `ai` and `bi` in the graph.

Return `true` _if the edges of the given graph make up a valid tree, and_ `false` _otherwise_.

```python
class Solution:
    """
    a tree has no cycles and every node has to be reachable in a single path
    """
    def validTree(self, n: int, edges: List[List[int]]) -> bool:
        g = collections.defaultdict(list)
        for a, b in edges:
            g[a].append(b)
            g[b].append(a)
        
        seen = set()
        def recurse(node, parent):
            for neighbor in g[node]:
                if neighbor == parent:
                    continue
                if neighbor in seen:
                    return False

                seen.add(neighbor)
                if not recurse(neighbor, node):
                    return False
            return True

        seen.add(0)
        return recurse(0, -1) and len(seen) == n
```

- a tree is defined as a graph that has no cycles, and contains a path that allows you to reach every node in the graph.
- we can just [[dfs]] or [[bfs]] starting from the first node, and keep track of the nodes that we’ve seen.
	- because the graph is bidirectional, we keep track of what the parent node is in each recursive call, so we don’t detect trivial cycles.
- at the end, if we never see a node that we’ve already seen, and we have visited every node, then we know that our graph is a valid tree.

Categories:: [[graph]], [[tree]], [[bfs]], [[dfs]]
