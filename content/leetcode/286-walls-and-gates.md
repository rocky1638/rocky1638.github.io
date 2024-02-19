---
created_at: 2023-01-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/walls-and-gates/
---

# 286. Walls And Gates

You are given an `m x n` grid `rooms` initialized with these three possible values.

- `-1` A wall or an obstacle.
- `0` A gate.
- `INF` Infinity means an empty room. We use the value `231 - 1 = 2147483647` to represent `INF` as you may assume that the distance to a gate is less than `2147483647`.

Fill each empty room with the distance to _its nearest gate_. If it is impossible to reach a gate, it should be filled with `INF`.

![](https://assets.leetcode.com/uploads/2021/01/03/grid.jpg)

```python
class Solution:
    def wallsAndGates(self, rooms: List[List[int]]) -> None:
        """
        - bfs in parallel from all the gates at once.
        - the first time each empty cell is reached, it must have been
          from the closest gate to it.
        - keep track of depth in bfs, fill in the cells.
        """
        INF = 2147483647
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]

        q = collections.deque()
        for i in range(len(rooms)):
            for j in range(len(rooms[i])):
                if rooms[i][j] == 0:
                    q.append((i, j, 0))

        while q:
            i, j, dist = q.popleft()
            for d in dirs:
                ni, nj = i + d[0], j + d[1]

                if ni >= 0 and ni < len(rooms) and nj >= 0 and nj < len(rooms[0]):
                    if rooms[ni][nj] == INF:
                        rooms[ni][nj] = dist + 1
                        q.append((ni, nj, dist + 1))
```

- we bfs in parallel from all of the gates.
- the first time we reach a cell, we must have reached it from the closest gate to it because all the traversals are moving outwards at the same rate.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[bfs]], [[matrix]]
