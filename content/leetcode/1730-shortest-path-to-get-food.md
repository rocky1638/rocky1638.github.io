# 1730. Shortest Path to Get Food

```python
class Solution:
    def getFood(self, grid: List[List[str]]) -> int:
        dirs = [[0,1], [1,0], [0,-1], [-1,0]]
        q = collections.deque() 
        visited = set([])

        for i, row in enumerate(grid):
            for j, cell in enumerate(row):
                if cell == '*':
                    q.append((i, j))
                    visited.add((i, j))
                    break
        l = 1
        while q:
            level_len = len(q)
            for _ in range(level_len):
                x, y = q.popleft()

                for d in dirs:
                    _x, _y = x + d[0], y + d[1] 
                    if _x >= 0 and _x < len(grid) and _y >= 0 and _y < len(grid[0]):
                        if (_x, _y) not in visited:
                            if grid[_x][_y] == 'O':
                                q.append((_x,_y))
                                visited.add((_x, _y))
                            elif grid[_x][_y] == '#':
                                return l
            l += 1
        return -1
```

- basic [[bfs]] problem through the [[matrix]].

[[array]]