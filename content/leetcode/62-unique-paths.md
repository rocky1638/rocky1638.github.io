---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/unique-paths/
---

# 62. Unique Paths

```python
class Solution:
    def uniquePaths(self, m: int, n: int) -> int:
        # we can use 2d dp
        # each square can be reached from either above or the left
        
        dp = [[0 for _ in range(n)] for _ in range(m)]
        dp[0][0] = 1
        
        for i in range(m):
            for j in range(n):
                above = 0
                left = 0
                
                if (i-1) >= 0:
                    above = dp[i-1][j]
                if (j-1) >= 0:
                    left = dp[i][j-1]
                dp[i][j] += above + left
        
        return dp[-1][-1]
```

- we can use [[dynamic-programming]], where in our `dp` array $dp[i][j]$ represents the number of ways to reach the cell $M[i][j]$.
- then, the number of ways to reach any cell is the total number of ways to reach the cell above and the number of ways to reach the cell to the left.

$$
	dp[i][j] = 
	\begin{cases}
	1, \text{ if } i=0 \text{ and } j=0, \\
	dp[i-1][j]+dp[i][j-1] \text{ otherwise.}
	\end{cases}
$$

Categories:: [[dynamic-programming]]
