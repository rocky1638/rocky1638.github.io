---
created_at: 2022-12-10
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/pacific-atlantic-water-flow/
---

# 417. Pacific Atlantic Water Flow

There is an `m x n` rectangular island that borders both the **Pacific Ocean** and **Atlantic Ocean**. The **Pacific Ocean** touches the island's left and top edges, and the **Atlantic Ocean** touches the island's right and bottom edges.

The island is partitioned into a grid of square cells. You are given an `m x n` integer matrix `heights` where `heights[r][c]` represents the **height above sea level** of the cell at coordinate `(r, c)`.

The island receives a lot of rain, and the rain water can flow to neighboring cells directly north, south, east, and west if the neighboring cell's height is **less than or equal to** the current cell's height. Water can flow from any cell adjacent to an ocean into the ocean.

Return _a **2D list** of grid coordinates_ `result` _where_ `result[i] = [ri, ci]` _denotes that rain water can flow from cell_ `(ri, ci)` _to **both** the Pacific and Atlantic oceans_.

![](https://assets.leetcode.com/uploads/2021/06/08/waterflow-grid.jpg)

```python
class Solution:
    def pacificAtlantic(self, heights: List[List[int]]) -> List[List[int]]:
        mat = [[0 for _ in range(len(heights[0]))] for _ in range(len(heights))]
        def bfs(starting_spots):
            dirs = [[0,1],[1,0],[-1,0],[0,-1]]
            q = collections.deque(starting_spots)

            while q:
                x, y = q.popleft()
                for d in dirs:
                    _x, _y = x + d[0], y + d[1]
                    # bound checks
                    if _x >= 0 and _x < len(heights) and _y >= 0 and _y < len(heights[0]):
                        if (_x, _y) not in seen:
                            # we have to move flat or uphill
                            if heights[_x][_y] >= heights[x][y]:
                                seen.add((_x, _y))
                                q.append([_x, _y])
                                # we've reached this cell from an ocean
                                mat[_x][_y] += 1

        # bfs from pacific ocean
        pacific = []
        seen = set()
        for i, row in enumerate(heights):
            for j, val in enumerate(row):
                if i == 0 or j == 0:
                    pacific.append([i, j])
                    seen.add((i, j))
                    mat[i][j] += 1
        bfs(pacific)

        # bfs from atlantic ocean
        atlantic = []
        seen.clear()
        for i, row in enumerate(heights):
            for j, val in enumerate(row):
                if i == len(heights)-1 or j == len(heights[0])-1:
                    atlantic.append([i, j])
                    seen.add((i, j))
                    mat[i][j] += 1
        bfs(atlantic)

        # go through mat and return all the cells that have a value of 2
        ans = []
        for i in range(len(mat)):
            for j in range(len(mat[i])):
                if mat[i][j] == 2:
                    ans.append([i, j])
        return ans
```

- we [[bfs]] from both of the coastlines, and if we reach a piece of land while moving uphill from the ocean, then we know that we can flow downhill to both coastlines from this block.
- use another [[matrix]] to keep track of if we reach specific cells from both coastlines.
- at the end, return the coordinates of all the cells that have been reached from both coastlines.

Categorie:: [[array]], [[bfs]], [[matrix]]
