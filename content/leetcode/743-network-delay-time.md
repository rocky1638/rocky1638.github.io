---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/network-delay-time/
---

# 743. Network Delay Time

You are given a network of `n` nodes, labeled from `1` to `n`. You are also given `times`, a list of travel times as directed edges `times[i] = (ui, vi, wi)`, where `ui` is the source node, `vi` is the target node, and `wi` is the time it takes for a signal to travel from source to target.

We will send a signal from a given node `k`. Return _the **minimum** time it takes for all the_ `n` _nodes to receive the signal_. If it is impossible for all the `n` nodes to receive the signal, return `-1`.

```python
class Solution:
    def networkDelayTime(self, times: List[List[int]], n: int, k: int) -> int:
        # create weighted directed graph as adjacency list
        edges = collections.defaultdict(list)
        for u, v, w in times:
            edges[u].append((v, w))

        # we start at node k, requires 0 time/weight
        minHeap = [(0, k)]
        visit = set()
        t = 0
        while minHeap:
            w1, n1 = heapq.heappop(minHeap)
            if n1 in visit:
                continue
            visit.add(n1)
            t = w1

            for n2, w2 in edges[n1]:
                if n2 not in visit:
                    heapq.heappush(minHeap, (w1 + w2, n2))
        return t if len(visit) == n else -1
```

- this problem is exactly the single-source-shortest-path (SSSP) problem, and can be solved with djikstra’s algorithm or the bellman-ford algorithm.
- we use a heap in our bfs through the graph and keep track of the weight it has taken to reach the current node.
	- always advance the bfs from the cheapest current path on the frontier.
	- keep a visited array.
- if we visit everything, then return the value of the smallest weight that we got after reaching all of the nodes.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

- https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm.
- https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford_algorithm.

Categories:: [[graph]], [[djikstra]], [[heap]]
