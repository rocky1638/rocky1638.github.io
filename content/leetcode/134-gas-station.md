---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/gas-station/
---

# 134. Gas Station

```python
class Solution:
    def canCompleteCircuit(self, gas, cost):
        n = len(gas)
        
        total_tank, curr_tank = 0, 0
        starting_station = 0
        for i in range(n):
            total_tank += gas[i] - cost[i]
            curr_tank += gas[i] - cost[i]
            # If one couldn't get here,
            if curr_tank < 0:
                # Pick up the next station as the starting one.
                starting_station = i + 1
                # Start with an empty tank.
                curr_tank = 0
        
        return starting_station if total_tank >= 0 else -1
```

- our first thought is to check each station as a starting point, and then return the one that allows us to go the whole way around the loop.
	- this takes $O(n^2)$ time.
- we realize that we don’t actually have to check every possible station in a loop.
	- consider the case in which we start at station $i$, and end up making it to some other station $j$.
		- we know that if we were to check again starting at station $i+1$, we would be guaranteed to have less than or equal to the same amount of gas going into station $i+2$ and onwards, because we are guaranteed to bring over a zero or positive amount of gas from $i$ to $i+1$.
		- therefore, we should just greedily decide to start at the next station from where we failed, because starting at any station in the path from $i$ to $j$ will also fail at station $j$.

Categories:: [[greedy]]
