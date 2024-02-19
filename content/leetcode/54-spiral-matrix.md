---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/spiral-matrix/
---

# 54. Spiral Matrix

```python
class Solution:
    def spiralOrder(self, matrix: List[List[int]]) -> List[int]:
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]
        # go in order of dirs, move to next direction once we see border or seen
        seen = set()
        ans = []
        cd = 0
        
        i, j = 0, 0
        
        for _ in range(len(matrix) * len(matrix[0])):
                ans.append(matrix[i][j])
                seen.add((i,j))
                
                ni, nj = i + dirs[cd][0], j + dirs[cd][1]
                if ni >= 0 and ni < len(matrix) and nj >= 0 and nj < len(matrix[0]) and (ni,nj) not in seen:
                        # if valid and unseen, move to it
                        i, j = ni, nj
                else:
                    cd = (cd + 1) % 4
                    ni, nj = i + dirs[cd][0], j + dirs[cd][1]
                    i, j = ni, nj
        
        return ans
```

- some basic but annoying [[matrix]] logic.

Categories:: [[array]], [[matrix]]
