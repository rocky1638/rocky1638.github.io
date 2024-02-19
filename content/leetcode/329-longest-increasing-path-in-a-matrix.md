# 329. Longest Increasing Path in a Matrix

```python
class Solution:
    def longestIncreasingPath(self, matrix: List[List[int]]) -> int:
        memo = [[None for _ in range(len(matrix[0]))] for _ in range(len(matrix))]

        depth = 1
        ans = 0
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]

        def dfs(x, y):
            nonlocal depth
            nonlocal ans
            nonlocal memo

            ans = max(ans, depth)
            # update memo if we improved
            if not memo[x][y] or depth > memo[x][y]:
                memo[x][y] = depth
            # there is already another dfs path that will check
            else:
                return

            for d in dirs:
                nx, ny = x + d[0], y + d[1]
                if nx >= 0 and nx < len(matrix) and ny >= 0 and ny < len(matrix[0]):
                    if matrix[nx][ny] > matrix[x][y]:
                        depth += 1
                        dfs(nx, ny)
                        depth -= 1

        for i in range(len(matrix)):
            for j in range(len(matrix[i])):
                dfs(i, j)
        return ans
```

- this first one is just [[recursion]] with [[memoization]] using [[dfs]].
- this is [[dynamic-programming]]?