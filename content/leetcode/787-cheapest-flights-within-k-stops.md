---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/cheapest-flights-within-k-stops/
---

# 787. Cheapest Flights Within K Stops

There are `n` cities connected by some number of flights. You are given an array `flights` where `flights[i] = [fromi, toi, pricei]` indicates that there is a flight from city `fromi` to city `toi` with cost `pricei`.

You are also given three integers `src`, `dst`, and `k`, return _**the cheapest price** from_ `src` _to_ `dst` _with at most_ `k` _stops._ If there is no such route, return `-1`.

![](https://assets.leetcode.com/uploads/2022/03/18/cheapest-flights-within-k-stops-3drawio.png)

```python
class Solution:
    def findCheapestPrice(self, n: int, flights: List[List[int]], src: int, dst: int, k: int) -> int:
        """
        - do a bfs with a priority queue on the current cost so far.
        - if our node is at max stops, k, and still haven't reached, continue.
        - always advance bfs from smallest cost path first.
        - first tuple we pop that has reached the dest is our return.
        """

        g = collections.defaultdict(list)
        for fr, to, prc in flights:
            g[fr].append((to, prc))

        # heap[i] = (weightsofar, stopssofar, node)
        # we start with the src, and no cost
        minHeap = [(0, -1, src)]
        # stop: (weight, num_stops)
        visited = {src: (0, -1)}

        while minHeap:
            w1, s1, n1 = heapq.heappop(minHeap)
            if n1 == dst and s1 <= k:
                return w1
            elif s1 > k:
                continue
            
            for neighbor, weight in g[n1]:
                if neighbor not in visited or visited[neighbor][0] >= w1+weight or visited[neighbor][1] > s1+1:
                    visited[neighbor] = (w1+weight, s1+1)
                    heapq.heappush(minHeap, (w1+weight, s1+1, neighbor))

        return -1
```

- we do a bfs with a priority queue to always advance our bfs to the cheapest next node first.
	- this guarantees that the first time we reach the destination, that is the cheapest path to reach it.
- in order to improve efficiency, we keep track of the optimal ways that we have reached each node so far.
	- we keep track of the weight and number of stops it took to reach each node.
	- **if we see a repeat node in our bfs, we only go to it if it improves on either the weight or the number of stops.**

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[graph]], [[bfs]], [[dynamic-programming]], [[heap]], [[priority-queue]]
