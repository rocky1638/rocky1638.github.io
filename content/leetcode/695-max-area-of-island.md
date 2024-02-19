---
created_at: 2023-01-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/max-area-of-island/
---

# 695. Max Area Of Island

You are given an `m x n` binary matrix `grid`. An island is a group of `1`'s (representing land) connected **4-directionally** (horizontal or vertical.) You may assume all four edges of the grid are surrounded by water.

The **area** of an island is the number of cells with a value `1` in the island.

Return _the maximum **area** of an island in_ `grid`. If there is no island, return `0`.

![](https://assets.leetcode.com/uploads/2021/05/01/maxarea1-grid.jpg)

```python
class Solution:
    def maxAreaOfIsland(self, grid: List[List[int]]) -> int:
        ans = 0
        dirs = [[0, 1], [1, 0], [0, -1], [-1, 0]]

        def dfs(i: int, j: int) -> int:
            if i >= 0 and i < len(grid) and j >= 0 and j < len(grid[0]):
                if grid[i][j] == 1:
                    # sink
                    grid[i][j] = 0

                    # recurse on neighbors 
                    rest = 0
                    for d in dirs:
                        ni, nj = i + d[0], j + d[1]
                        rest += dfs(ni, nj)
                    return 1 + rest
                return 0

            else:
                return 0
        
        for i in range(len(grid)):
            for j in range(len(grid[0])):
                if grid[i][j] == 1:
                    ans = max(ans, dfs(i, j))
        return ans
```

- we just do a dfs on the areas that have a 1, sink islands that we already visit, and keep track of the biggest island.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[200-number-of-islands]].

## References.

Categories:: [[dfs]], [[matrix]]
