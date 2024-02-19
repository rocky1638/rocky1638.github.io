# 308. Range Sum Query 2D - Mutable

```python
class NumMatrix:
    def __init__(self, matrix: List[List[int]]):
        self.matrix = matrix
        
        # self.prefixes[row][index] = sum of prefix array up to and including index
        self.prefixes = []
        # calculate prefix sums per row
        for i, row in enumerate(matrix):
            acc = 0
            prefixes = []
            
            for num in row:
                acc += num
                prefixes.append(acc)
            self.prefixes.append(prefixes)

    def update(self, row: int, col: int, val: int) -> None:
        diff = val - self.matrix[row][col]
        self.matrix[row][col] = val
        self.prefixes[row][col] += diff
        for j in range(col+1, len(self.matrix[row])):
            self.prefixes[row][j] += diff

    def sumRegion(self, row1: int, col1: int, row2: int, col2: int) -> int:
        ret = 0
        for r in range(row1, row2 + 1):
            row_sum = 0
            if col1 == 0:
                row_sum = self.prefixes[r][col2]
            else:
                row_sum = self.prefixes[r][col2] - self.prefixes[r][col1-1]
            ret += row_sum
        return ret


# Your NumMatrix object will be instantiated and called as such:
# obj = NumMatrix(matrix)
# obj.update(row,col,val)
# param_2 = obj.sumRegion(row1,col1,row2,col2)
```

- use the [[prefix-sum]] pattern to reduce the time complexity of `sumRegion()` from $O(n^2)$ to $O(n)$.
- `update()` is slower, from $O(1)$ to $O(n)$, but assuming similar rates of each function, I’d rather have two $O(n)$ then one $O(n^2)$.

Categories:: [[matrix]], [[array]], [[prefix-sum]]
