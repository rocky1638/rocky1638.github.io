---
created_at: 2023-01-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/redundant-connection/
---

# 684. Redundant Connection

In this problem, a tree is an **undirected graph** that is connected and has no cycles.

You are given a graph that started as a tree with `n` nodes labeled from `1` to `n`, with one additional edge added. The added edge has two **different** vertices chosen from `1` to `n`, and was not an edge that already existed. The graph is represented as an array `edges` of length `n` where `edges[i] = [ai, bi]` indicates that there is an edge between nodes `ai` and `bi` in the graph.

Return _an edge that can be removed so that the resulting graph is a tree of_ `n` _nodes_. If there are multiple answers, return the answer that occurs last in the input.

```python
class UnionFind:
    def __init__(self, n):
        self.parent = [i for i in range(n)]
        self.size = [1] * n
        
    def find(self, x):
        if x != self.parent[x]:
            self.parent[x] = self.find(self.parent[x]) # Path compression
        return self.parent[x]
    
    def union(self, u, v):
        pu, pv = self.find(u), self.find(v)
        if pu == pv: return False  # Return False if u and v are already union
        if self.size[pu] > self.size[pv]: # Union by larger size
            self.size[pu] += self.size[pv]
            self.parent[pv] = pu
        else:
            self.size[pv] += self.size[pu]
            self.parent[pu] = pv
        return True

class Solution:
    def findRedundantConnection(self, edges: List[List[int]]) -> List[int]:
        """
        - perform union find operation, first edge that we try to add
          between nodes that are already in the same set is our answer.
        - being fully connected with n-1 nodes and one extra edge, there
          are guaranteed to be n edges.
            - so, we can initialize our union find with n nodes.
        """
        uf = UnionFind(len(edges))
        
        for n1, n2 in edges:
            # convert to 0-indexing
            if not uf.union(n1-1, n2-1):
                return [n1, n2]
```

- explained in the docstring.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[721-accounts-merge]].

## References.

Categories:: [[graph]], [[union-find]]
