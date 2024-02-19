---
created_at: 2022-12-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/
---

# 323. Number of Connected Components in an Undirected Graph

You have a graph of `n` nodes. You are given an integer `n` and an array `edges` where `edges[i] = [ai, bi]` indicates that there is an edge between `ai` and `bi` in the graph.

Return _the number of connected components in the graph_.

```python
class Solution:
    def countComponents(self, n: int, edges: List[List[int]]) -> int:
        seen = set()

        # create graph
        g = {}
        for node in range(n):
            g[node] = []
        for n1, n2 in edges:
            g[n1].append(n2)
            g[n2].append(n1)

        def bfs(node):
            nonlocal g
            nonlocal seen
            q = collections.deque([node])
            while q:
                cur = q.popleft()
                for neighbor in g[cur]:
                    if neighbor not in seen:
                        q.append(neighbor)
                        seen.add(neighbor)

        ans = 0
        for node in range(n):
            if node not in seen:
                bfs(node)
                ans += 1
        return ans
```

- we loop through the nodes in the graph, and do standard [[bfs]] through the [[graph]] from nodes if they are not yet seen.
- everytime we have to initiate a bfs search from an unseen node, we know that that is a connected component, because if was part of another component we would have already seen it in an earlier bfs.

Categories:: [[bfs]], [[graph]]
