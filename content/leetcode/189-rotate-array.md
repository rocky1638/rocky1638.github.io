# 189. Rotate Array

```python
class Solution:
    def rotate(self, nums: List[int], k: int) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """

        n = len(nums)
        k = k % n

        num_moved = 0
        current_idx = 0
        to_write = nums[0]
        start_idx = 0

        while num_moved < n:
            current_idx, to_write = start_idx, nums[start_idx]
            while True:
                next_idx = (current_idx + k) % n
                nums[next_idx], to_write = to_write, nums[next_idx]
                current_idx = next_idx
                num_moved += 1

                if next_idx == start_idx:
                    break

            # if we cycle back to the start and haven't
            # moved everything, then we are guaranteed that the next
            # idx has not been moved yet. (If it had been moved, k == 2)
            start_idx += 1
```

- we cyclically rotate the [[array]] in-place.
- if `k` is a non-one factor of the length of the array, then we will return to the original element without swapping every value in the array.
	- when this happens, we know that the next element is not yet moved, because if it were, then either $k = 2$ or $k$ must have been a relative prime of $n$.