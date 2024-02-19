---
created_at: 2022-12-29
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/search-a-2d-matrix/
---

# 74. Search a 2D Matrix

You are given an `m x n` integer matrix `matrix` with the following two properties:

- Each row is sorted in non-decreasing order.
- The first integer of each row is greater than the last integer of the previous row.

Given an integer `target`, return `true` _if_ `target` _is in_ `matrix` _or_ `false` _otherwise_.

You must write a solution in `O(log(m * n))` time complexity.

## Linear scan.

```python
class Solution:
    def searchMatrix(self, matrix: List[List[int]], target: int) -> bool:
        # start at bottom-left
        i, j = len(matrix)-1, 0

        while i >= 0 and j < len(matrix[0]):
            val = matrix[i][j]
            if val == target:
                return True
            elif val < target:
                j += 1
            else:
                i -= 1
        return False
```

- we know the matrix is sorted left-right and up-down.
- so, to find a number we can constrain our options at each step to just one.
	- if we start at the bottom-left, we know that given any number, if we need to go bigger, we have to go to the right, and if we need to go smaller, we have to go up.
	- this makes it a $O(m+n)$ search.

## Two binary searches.

```python
class Solution:
    def searchMatrix(self, matrix: List[List[int]], target: int) -> bool:
        # find the row the number would be in with binary search
        l, r = 0, len(matrix)-1
        row_idx = None
        while l <= r:
            m = (l+r)//2
            
            if matrix[m][0] <= target <= matrix[m][-1]:
                row_idx = m
                break
            elif matrix[m][0] > target:
                r = m - 1
            else:
                l = m + 1

        if row_idx is None: return False

        # binary search the row
        a = matrix[row_idx]
        l, r = 0, len(a)-1

        while l <= r:
            m = (l+r)//2

            if a[m] == target:
                return True
            elif a[m] > target:
                r = m - 1
            else:
                l = m + 1

        return False
```

- we use binary search first to find the row in which the `target` should appear.
- then, we perform binary search again on this row to find the number.
- the runtime is $O(\log m + \log n) \equiv O(\log mn)$.

Categories:: [[matrix]], [[binary-search]], [[array]]
