# 268. Missing Number

```python
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        # increment by one to avoid 0 corner case
        nums = [x+1 for x in nums]
        n = len(nums)
        
        for i, num in enumerate(nums):
            to_idx = abs(num)-1
            if to_idx < n:
                nums[to_idx] *= -1

        for i in range(len(nums)):
            if nums[i] > 0:
                return i
        return n
```

- we mark the numbers that we find in-place by setting the values at the indices of the number to negative.
	- we can do this because the range of numbers is set to $[1,n]$.
	- to avoid the case where we can’t set 0 to be negative, we first just increment every value in the array by 1.

[[array]]