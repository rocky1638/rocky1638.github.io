---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/sort-colors/
---

# 75. Sort Colors

```python
class Solution:
    def sortColors(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        zero_idx = 0
        two_idx = len(nums)-1
        
        i = 0
        while i <= two_idx:
            if nums[i] == 0:
                nums[zero_idx], nums[i] = nums[i], nums[zero_idx]
                if zero_idx == i:
                    i += 1
                zero_idx += 1
            elif nums[i] == 2:
                nums[two_idx], nums[i] = nums[i], nums[two_idx]
                two_idx -= 1
            else:
                i += 1
```

- we sort in-place by keeping track of where we are with putting zeroes in the front and twos in the back.
- there is some weird off-by-one logic that has to be done to make sure everything works, just review it.

Categories:: [[sorting]], [[two-pointers]], [[array]]
