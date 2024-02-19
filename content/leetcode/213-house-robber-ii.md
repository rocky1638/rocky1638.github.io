---
created_at: 2023-01-14
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/house-robber-ii/
---

# 213. House Robber II

You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed. All houses at this place are **arranged in a circle.** That means the first house is the neighbor of the last one. Meanwhile, adjacent houses have a security system connected, and **it will automatically contact the police if two adjacent houses were broken into on the same night**.

Given an integer array `nums` representing the amount of money of each house, return _the maximum amount of money you can rob tonight **without alerting the police**_.

```python
class Solution:
    def rob(self, nums: List[int]) -> int:
        """
        - if we rob the first house, we can't rob the last house
        - run two dps, one where we always skip the first house
          one where we always take from the first house
        - max of the last house from the skipping first house dp
          and the second last house from the taking first house dp
        """
        if len(nums) == 1:
            return nums[0]
        if len(nums) == 2:
            return max(nums[0], nums[1])

        take_dp = [nums[0], nums[0]]
        for i in range(2, len(nums)-1):
            take_dp.append(max(take_dp[i-1], nums[i]+take_dp[i-2]))

        skip_dp = [0, nums[1]]
        for i in range(2, len(nums)):
            skip_dp.append(max(skip_dp[i-1], nums[i]+skip_dp[i-2]))

        return max(take_dp[-1], skip_dp[-1])
```

- consider two cases where we either take the first house or not.
	- if we take the first house, we can’t consider the last house, and vice versa.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[dynamic-programming]], [[array]]
