# 283. Move Zeroes

```python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        leftmost_zero, leftmost_nonzero = None, None

        for i in range(len(nums)):
            if leftmost_nonzero is not None and leftmost_zero is not None:
                break
            if nums[i] == 0 and leftmost_zero is None:
                leftmost_zero = i
                # we want the leftmost nonzero that is after a 0
                # (anything before a 0 does not need swapping)
                leftmost_nonzero = None
            if nums[i] != 0 and leftmost_nonzero is None:
                leftmost_nonzero = i

        if leftmost_nonzero is None or leftmost_zero is None:
            return
        if leftmost_nonzero < leftmost_zero:
            return

        while leftmost_zero < len(nums) and leftmost_nonzero < len(nums):
            # swap
            nums[leftmost_zero], nums[leftmost_nonzero] = nums[leftmost_nonzero], nums[leftmost_zero]

            leftmost_zero += 1
            while leftmost_zero < len(nums) and nums[leftmost_zero] != 0:
                leftmost_zero += 1

            leftmost_nonzero += 1
            while leftmost_nonzero < len(nums) and nums[leftmost_nonzero] == 0:
                leftmost_nonzero += 1
```

- we use a [[two-pointers]] strategy to swap zeroes to the back of the [[array]].
- keep track of where the leftmost zero is, and where the leftmost nonzero that is *to the right* of a zero is.
	- we don’t need to worry about nonzero numbers that are before any zero, because they do not need to be moved in any way.