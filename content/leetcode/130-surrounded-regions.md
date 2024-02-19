---
created_at: 2023-01-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/surrounded-regions/
---

# 130. Surrounded Regions

Given an `m x n` matrix `board` containing `'X'` and `'O'`, _capture all regions that are 4-directionally surrounded by_ `'X'`.

A region is **captured** by flipping all `'O'`s into `'X'`s in that surrounded region.

![](https://assets.leetcode.com/uploads/2021/02/19/xogrid.jpg)

```python
class Solution:
    def solve(self, board: List[List[str]]) -> None:
        """
        - We find the islands that don't touch an edge.
        - First go around the edges, and mark the islands that
          touch an edge as safe using a sentinel value.
        - Then, look through the non-edges for islands to sink.
        """
         
        dirs = [[0, 1], [1, 0], [0, -1], [-1, 0]]
        m, n = len(board), len(board[0])

        def dfs(i, j, fill_char="8"):
            if i >= 0 and i < m and j >= 0 and j < n:
                if board[i][j] == "O":
                    board[i][j] = fill_char

                    for d in dirs:
                        ni, nj = i + d[0], j + d[1]
                        dfs(ni, nj, fill_char=fill_char)
        
        # mark islands that shouldn't be sunk
        for i in range(m):
            for j in range(n):
                # edges
                if i == 0 or j == 0 or i == m-1 or j == n-1:
                    dfs(i, j)

        # sink islands
        for i in range(m):
            for j in range(n):
                # not edges
                if not(i == 0 or j == 0 or i == m-1 or j == n-1):
                    dfs(i, j, fill_char="X")

        # replace sentinel value with original island
        for i in range(m):
            for j in range(n):
                if board[i][j] == "8":
                    board[i][j] = "O"
```

- we know all “islands” will only be enclosed if they do not touch the edge of the matrix.
- we first mark all the islands that touch an edge with a sentinel value, then sink the other islands.
- at the end, we replace the sentinel value back with the original “O”.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[200-number-of-islands]].

## References.

Categories:: [[dfs]], [[matrix]], [[array]]
