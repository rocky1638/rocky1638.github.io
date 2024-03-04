---
title: 62. unique paths
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/unique-paths/
date: 2022-11-22
updated: 2024-03-03
tags:
  - dp
---

There is a robot on an `m x n` grid. The robot is initially located at the **top-left corner** (i.e., `grid[0][0]`). The robot tries to move to the **bottom-right corner** (i.e., `grid[m - 1][n - 1]`). The robot can only move either down or right at any point in time.

Given the two integers `m` and `n`, return _the number of possible unique paths that the robot can take to reach the bottom-right corner_.

The test cases are generated so that the answer will be less than or equal to `2 * 109`.

## solution

We can use dynamic programming, where in our `dp` array $dp[i][j]$ represents the number of ways to reach the cell $M[i][j]$.

Then, the number of ways to reach any cell is the total number of ways to reach the cell above and the number of ways to reach the cell to the left.

$$
	dp[i][j] = 
	\begin{cases}
	1, \text{ if } i=0 \text{ and } j=0, \\
	dp[i-1][j]+dp[i][j-1] \text{ otherwise.}
	\end{cases}
$$

```python
def uniquePaths(self, m: int, n: int) -> int:
	# we can use 2d dp
	# each square can be reached from either above or the left
  
	dp = [[0 for j in range(n)] for i in range(m)]
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
