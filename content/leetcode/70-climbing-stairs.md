---
created_at: 2022-11-13
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/climbing-stairs/
---

# 70. Climbing Stairs

```python
class Solution:
    def climbStairs(self, n: int) -> int:
        if n == 1:
            return 1
        
        dp = [1, 2]
        
        for i in range(2, n):
            num_ways = dp[i-1] + dp[i-2]
            dp.append(num_ways)
        
        return dp[-1]
```

- simple [[dynamic-programming]].
- you can reach the next step by either going from one or two steps below, so the number of ways to reach step `n` is the number of ways to reach step `n-1` and the number of ways to reach step `n-2`.

Categories:: [[dynamic-programming]]
