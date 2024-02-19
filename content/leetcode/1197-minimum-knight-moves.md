# 1197. Minimum Knight Moves

## Basic exhaustive [[bfs]].
```python
class Solution:
    def minKnightMoves(self, x: int, y: int) -> int:
        dirs = [[-2,-1],[2,1],[-2,1],[2,-1],[1,2],[-1,-2],[-1,2],[1,-2]]

        q = collections.deque([(0, 0)])
        seen = set()
        level = 0

        while q:
            level_len = len(q)
            for _ in range(level_len):
                i, j = q.popleft()
                if i == x and j == y:
                    return level
                for d in dirs:
                    ni, nj = i + d[0], j + d[1]
                    if (ni, nj) not in seen:
                        q.append((ni, nj))
                        seen.add((ni, nj))
            level += 1
```

- we do a normal level-order [[bfs]] and return the level when we reach the desired target square.
![[1197-e1.excalidraw]]

## Two-way [[bfs]] from start and target.
```python
class Solution:
    def minKnightMoves(self, x: int, y: int) -> int:
        if x == y == 0:
            return 0
            
        dirs = [[-2,-1],[2,1],[-2,1],[2,-1],[1,2],[-1,-2],[-1,2],[1,-2]]

        qs = collections.deque([(0, 0)])
        qt = collections.deque([(x, y)])

        # every time we see, store
        # the distance from start/target
        seen_from_start = {}
        seen_from_target = {}

        level = 0

        # level by level bfs from start and target in lockstep
        while qs and qt:
            qs_level_len = len(qs)
            for _ in range(qs_level_len):
                i, j = qs.popleft()
                if (i, j) in seen_from_target:
                    return level + seen_from_target[(i, j)] + 1
                for d in dirs:
                    ni, nj = i + d[0], j + d[1]
                    if (ni, nj) not in seen_from_start:
                        qs.append((ni, nj))
                        seen_from_start[(ni, nj)] = level

            qt_level_len = len(qt)
            for _ in range(qt_level_len):
                i, j = qt.popleft()
                if (i, j) in seen_from_start:
                    return level + seen_from_start[(i, j)] + 1
                for d in dirs:
                    ni, nj = i + d[0], j + d[1]
                    if (ni, nj) not in seen_from_target:
                        qt.append((ni, nj))
                        seen_from_target[(ni, nj)] = level

            level += 1
```

- because our [[bfs]] essentially moves in a circle, if we start from target and start, we save a lot of search space because we search two smaller circles.
![[1197-e2.excalidraw]]

## Optimized [[dfs]].

```python
class Solution:
    def minKnightMoves(self, x: int, y: int) -> int:

        @lru_cache(maxsize=None)
        def dfs(x, y):
            if x + y == 0:
                # base case: (0, 0)
                return 0
            elif x + y == 2:
                # base case: (1, 1), (0, 2), (2, 0)
                return 2
            else:
                return min(
	                dfs(abs(x - 1), abs(y - 2)),
	                dfs(abs(x - 2), abs(y - 1))
				) + 1

        return dfs(abs(x), abs(y))
```

- we can actually also just [[dfs]] in solely the positive direction, because we know that a knight’s moves are four-way symmetrical.
	- just convert the target square to the (positive, positive) quadrant.
	- [[dfs]] from it towards the origin point.
	- handle edge cases for coordinates $(1,1)$, $(2,0)$ and $(0,2)$.