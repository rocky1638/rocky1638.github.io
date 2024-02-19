# 542. 01 Matrix

```python
from collections import deque

class Solution:
    def updateMatrix(self, mat: List[List[int]]) -> List[List[int]]:
        # bfs from all zeroes in parallel!
        
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]
        
        # first enqueue all the zeroes so we can bfs out from them
        # all in parallel
        q = deque()
        for i in range(len(mat)):
            for j in range(len(mat[0])):
                if mat[i][j] == 0:
                    q.append((i,j))
                else:
                    mat[i][j] = -1
        
        # now, when we bfs, the first time we reach a cell (when it is -1)
        # will be the closest distance it is from a zero
        while q:
            i, j = q.popleft()
            for d in dirs:
                ni, nj = i+d[0], j+d[1]
                if ni < 0 or ni == len(mat) or nj < 0 or nj == len(mat[0]) or mat[ni][nj] != -1: continue
                mat[ni][nj] = mat[i][j] + 1
                q.append((ni,nj))

        return mat
```

- we conduct a [[bfs]] from all the zero nodes in parallel.
- because all the branches of [[bfs]] coming off of the zeroes work in parallel, the first time we reach a new node *(marked with a value of -1)*, the value that we set for it is guaranteed to be the shortest distance between it and a zero node.
- in the diagram below, all the black arrow paths are conducted first before all the orange ones.

![[542-e1.excalidraw]]
[[dynamic-programming]], [[array]], [[matrix]]