---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/reconstruct-itinerary/
---

# 332. Reconstruct Itinerary

You are given a list of airline `tickets` where `tickets[i] = [fromi, toi]` represent the departure and the arrival airports of one flight. Reconstruct the itinerary in order and return it.

All of the tickets belong to a man who departs from `"JFK"`, thus, the itinerary must begin with `"JFK"`. If there are multiple valid itineraries, you should return the itinerary that has the smallest lexical order when read as a single string.

- For example, the itinerary `["JFK", "LGA"]` has a smaller lexical order than `["JFK", "LGB"]`.

You may assume all tickets form at least one valid itinerary. You must use all the tickets once and only once.

```python
class Solution:
    def findItinerary(self, tickets: List[List[str]]) -> List[str]:
        """
        - create adjacency list graph.
        - dfs from all tickets starting at JFK.
            - keep track of tickets that we've already used.
            - keep track of how long our path is.
            - break if the path length is equal
              to the number of tickets + 1.
        """
        tickets.sort()
        g = collections.defaultdict(collections.deque)
        for src, dest in tickets:
            g[src].append(dest)

        res = ["JFK"]
        def dfs(cur):
            nonlocal res
            
            if len(res) - 1 == len(tickets):
                return True

            for neighbor in list(g[cur]):
                g[cur].popleft()
                res.append(neighbor)
                if dfs(neighbor):
                    return True
                # after an invalid path, we want to use
                # the ticket again for some future path.
                res.pop()
                g[cur].append(neighbor)

        dfs("JFK")
        return res
```

- we create a graph, and then dfs down until we complete a valid itinerary.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[sorting]], [[dfs]], [[graph]], [[recursion]]
