---
created_at: 2023-01-14
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/min-cost-climbing-stairs/description/
---

# 746. Min Cost Climbing Stairs

You are given an integer array `cost` where `cost[i]` is the cost of `ith` step on a staircase. Once you pay the cost, you can either climb one or two steps.

You can either start from the step with index `0`, or the step with index `1`.

Return _the minimum cost to reach the top of the floor_.

```python
class Solution:
    def minCostClimbingStairs(self, cost: List[int]) -> int:
        # dp[i] is the min cost to reach step i
        dp = [0, 0]

        for i in range(2, len(cost)+1):
            dp.append(min(
                dp[i-1] + cost[i-1],
                dp[i-2] + cost[i-2]
            ))
        return dp[-1]
```

- we just do normal dp.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[70-climbing-stairs]].

## References.

Categories:: [[dynamic-programming]], [[array]]
