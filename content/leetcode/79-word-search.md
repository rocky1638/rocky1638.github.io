---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/word-search/
---

# 79. Word Search

```python
class Solution:
    def exist(self, board: List[List[str]], word: str) -> bool:
        found = False
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]
        visited = set()
        
        def dfs(i, j, word_idx):
            nonlocal found
            if word_idx == len(word)-1:
                found = True
                return
            
            for d in dirs:
                ni, nj = i + d[0], j + d[1]
                if ni >= 0 and ni < len(board) and nj >= 0 and nj < len(board[0]):
                    if (ni,nj) not in visited and board[ni][nj] == word[word_idx+1]:
                        visited.add((ni,nj))
                        dfs(ni, nj, word_idx+1)
                        visited.remove((ni,nj))
            
        for i in range(len(board)):
            for j in range(len(board[0])):
                if board[i][j] == word[0]:
                    visited.add((i,j))
                    dfs(i, j, 0)
                    visited.remove((i,j))
        return found
```

- this is a pretty classic [[dfs]] problem.
- we go through each character in the grid, and when we see a valid starting character, [[dfs]] through the entire grid to try to complete the target `word`.
- keep a visited set that we `add` and `remove` from *(when we backtrack)* between `dfs` calls.

Categories:: [[dfs]], [[backtracking]], [[array]], [[matrix]]
