# 1029. Two City Scheduling

```python
class Solution:
    def twoCitySchedCost(self, costs: List[List[int]]) -> int:
        # sort by difference in flight costs, descending
        # for example, if someone's costs are [1000, 1], we DEFINITELY
        # want them to fly to city b
            # it is most important to place this person in city b first (before it fills up)
            # because we really don't want them going to city a
        
        sorted_costs = sorted(costs, key=lambda x: -abs(x[0]-x[1]))
        
        ans = 0
        n = len(costs) / 2
        na = 0
        nb = 0
        
        for ca, cb in sorted_costs:
            if (na < n and ca <= cb) or nb == n:
                ans += ca
                na += 1
            elif (nb < n and cb <= ca) or na == n:
                ans += cb
                nb += 1
        return ans
```

- we take a [[greedy]] approach to “filling up” the two cities.
- the intuition is basically,
> which person do we “gain” the most from when choosing to put them in city a or city b?
- the answer is that we gain the most from choosing someone when the difference in cost for the person is greatest *(alternatively, because we end up wasting the most money if we end up putting them in the more expensive city)*.

[[array]], [[sorting]]