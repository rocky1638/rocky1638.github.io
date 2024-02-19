# 310. Minimum Height Trees

```python
class Solution:
    def findMinHeightTrees(self, n: int, edges: List[List[int]]) -> List[int]:
        if n == 1:
            return [0]
        
        if n == 2:
            return [0,1]
        
        # create graph
        g = defaultdict(set)
        # leaves have num_neighbors = 1
        num_neighbors = Counter()
        
        for n1, n2 in edges:
            num_neighbors[n1] += 1
            num_neighbors[n2] += 1
            g[n1].add(n2)
            g[n2].add(n1)
            
        leaves = []
        for key in num_neighbors:
            if num_neighbors[key] == 1:
                leaves.append(key)
        
        # using indegrees, we "prune" from the outside of the tree graph
        # whatever's left over is the center of the graph, and must be the roots
            # of any MHT (just like how shortest distance from edge in a circle is in the center)
        nodes_remaining = n
        q = deque(leaves)
        
        # there are either one or two central nodes
        # we use a topsort method to prune leaves layer by layer
        while nodes_remaining > 2 and q:
            level_len = len(q)
            
            for _ in range(level_len):
                cur = q.popleft()

                for neighbor in g[cur]:
                    # break edge
                    g[neighbor].remove(cur)
                    # update num_neighbors
                    num_neighbors[neighbor] -= 1
                    if num_neighbors[neighbor] == 1:
                        q.append(neighbor)

                nodes_remaining -= 1
                del num_neighbors[cur]
                del g[cur]
        
        return list(g.keys())
```

- the key realization here is that if we allow the nodes of the tree to sort out into a circular arrangement with the leaves at the outside *(just like the obsidian graph)*, then the roots of the MHTs must be in the center of the circle.
- we can also prove that there must be either one or two central nodes *(and no more)*.
- to find these node(s), we can progressively remove layers of leaves from the outside of the circle using a [[topological-sort]] strategy *(by keeping track of the number of edges that each node has)*.

[[tree]], [[graph]], [[bfs]]