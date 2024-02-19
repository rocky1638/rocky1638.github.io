# 1570. Dot Product of Two Sparse Vectors

```python
class SparseVector:
    def __init__(self, nums: List[int]):
        self.vals = {}
        
        for i, num in enumerate(nums):
            if num != 0:
                self.vals[i] = num

    # Return the dotProduct of two sparse vectors
    def dotProduct(self, vec: 'SparseVector') -> int:
        ans = 0
        # if only one is sparse, iterate through the sparse vector's vals
        for key in self.vals:
            if key in vec.vals:
                ans += self.vals[key] * vec.vals[key]
        return ans
```

- keep the non-zero values in a [[hashmap]] for more efficient storage.
- when doing the dot product, iterate through the more sparse vector and check if the index in the other vector is also non-zero.

[[math]]