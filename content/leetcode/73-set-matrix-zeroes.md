---
created_at: 2023-01-01
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/set-matrix-zeroes/
---

# 73 Set Matrix Zeroes

```python
class Solution:
    def setZeroes(self, matrix: List[List[int]]) -> None:
        seenRows = set()
        seenCols = set()

        def zeroCross(x, y):
            # clear row
            if x not in seenRows:
                for i in range(len(matrix[x])):
                    if matrix[x][i] != 0:
                        matrix[x][i] = None
                seenRows.add(x)
            
            # clear col
            if y not in seenCols:
                for j in range(len(matrix)):
                    if matrix[j][y] != 0:
                        matrix[j][y] = None
                seenCols.add(y)


        for i in range(len(matrix)):
            for j in range(len(matrix[i])):
                if matrix[i][j] == 0:
                    matrix[i][j] = None
                    zeroCross(i, j)

        for i in range(len(matrix)):
            for j in range(len(matrix[i])):
                if matrix[i][j] is None:
                    matrix[i][j] = 0
```

- we use a sentinel value to mark values as being cleared in place.
- we also use sets to keep track of rows/columns that we’ve already cleared so we don’t repeat operations.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[matrix]]
