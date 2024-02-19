# 311. Sparse Matrix Multiplication

## Matrix multiplication only when `mat1` value is non-zero.

```python
class Solution:
    def multiply(self, mat1: List[List[int]], mat2: List[List[int]]) -> List[List[int]]:
        
        # Product matrix.
        ans = [[0] * len(mat2[0]) for _ in range(len(mat1))]
        
        # for each row in mat1
        for mat1_row_idx, row in enumerate(mat1):
            for mat2_col_idx, mat2_val in enumerate(mat2[0]):
                for i, mat1_element in enumerate(row):
                    if mat1_element != 0:
                        ans[mat1_row_idx][mat2_col_idx] += mat1_element * mat2[i][mat2_col_idx]
        return ans
```

- doesn’t really take advantage of the sparse nature of the matrices.

## Compress data using [[hashmap]].

```python
class Solution:
    def multiply(self, mat1: List[List[int]], mat2: List[List[int]]) -> List[List[int]]:
        def compress_matrix(matrix: List[List[int]]) -> List[List[int]]:
            rows, cols = len(matrix), len(matrix[0])
            compressed_matrix = [[] for _ in range(rows)]
            for row in range(rows):
                for col in range(cols):
                    if matrix[row][col]:
                        compressed_matrix[row].append([matrix[row][col], col])
            return compressed_matrix
        
        m = len(mat1)
        k = len(mat1[0])
        n = len(mat2[0])
        
        # Store the non-zero values of each matrix.
        A = compress_matrix(mat1)
        B = compress_matrix(mat2)
        
        ans = [[0] * n for _ in range(m)]
        
        for mat1_row in range(m):
            # Iterate on all current 'row' non-zero elements of mat1.
            for element1, mat1_col in A[mat1_row]:
                # Multiply and add all non-zero elements of mat2
                # where the row is equal to col of current element of mat1.
                for element2, mat2_col in B[mat1_col]:
                    ans[mat1_row][mat2_col] += element1 * element2
                    
        return ans
```

- ![](https://leetcode.com/problems/sparse-matrix-multiplication/Figures/311/Slide31.PNG)
- compress the sparse matrices by saving only non-zero values in a [[hashmap]] keyed by row number, and store them as tuples of `(value, column)`.
- this is the response to if we can’t fit these giant matrices into memory, for example.

[[math]], [[matrix]]