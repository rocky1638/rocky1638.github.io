---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/number-of-islands/
---

# 200. Number of Islands

Given an `m x n` 2D binary grid `grid` which represents a map of `'1'`s (land) and `'0'`s (water), return _the number of islands_.

An **island** is surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You may assume all four edges of the grid are all surrounded by water.

```python
class Solution:
    def numIslands(self, grid: List[List[str]]) -> int:
        ans = 0
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]
        
        def sink(x, y):
            grid[x][y] = 'x'
            
            for d in dirs:
                nx, ny = x + d[0], y + d[1]
                if nx >= 0 and nx < len(grid) and ny >= 0 and ny < len(grid[0]):
                    if grid[nx][ny] == '1':
                        sink(nx, ny)
            
        for i in range(len(grid)):
            for j in range(len(grid[0])):
                if grid[i][j] == '1':
                    ans += 1
                    sink(i, j)
        return ans
```

- classic [[graph]] problem, you can use either [[dfs]] or [[bfs]] to traverse the islands and sink them.

Categories:: [[recursion]], [[matrix]], [[graph]], [[dfs]]
