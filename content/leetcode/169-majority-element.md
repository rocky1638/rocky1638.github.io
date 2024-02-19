# 169. Majority Element

```python
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        nums.sort()
        return nums[len(nums)//2]
```

- because we sort the array, the majority element will be guaranteed to be in the middle of the [[array]].

[[sorting]]