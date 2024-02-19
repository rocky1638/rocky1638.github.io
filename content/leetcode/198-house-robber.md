---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/house-robber/
---

# 198. House Robber

You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed, the only constraint stopping you from robbing each of them is that adjacent houses have security systems connected and **it will automatically contact the police if two adjacent houses were broken into on the same night**.

Given an integer array `nums` representing the amount of money of each house, return _the maximum amount of money you can rob tonight **without alerting the police**_.

```python
class Solution:
    def rob(self, nums: List[int]) -> int:
        if len(nums) == 1:
            return nums[0]
        if len(nums) == 2:
            return max(nums[0], nums[1])
        
        dp = [nums[0], max(nums[0], nums[1])] 

        for i in range(2, len(nums)):
            dp.append(max(dp[i-1], dp[i-2] + nums[i]))
        return dp[-1]
```

- basic [[dynamic-programming]] problem.
- at each house, we can either rob the house, meaning we have to take the maximum profit from two houses ago, or we can not rob the current house and take the maximum from the previous house.

Categories:: [[array]], [[dynamic-programming]]
