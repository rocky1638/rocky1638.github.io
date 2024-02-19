---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/partition-equal-subset-sum/
---

# 416. Partition Equal Subset Sum

Given an integer array `nums`, return `true` _if you can partition the array into two subsets such that the sum of the elements in both subsets is equal or_ `false` _otherwise_.

```python
class Solution:
    def canPartition(self, nums: List[int]) -> bool:
        # we just need to find if some subset of the nums can sum to 
        # half the total sum of nums
        
        s = sum(nums)
        if s % 2 == 1:
            return False
        
        half = s // 2
        
        # dp[i][j] = if sum j can be added up to with numbers from nums[:i]
        # for memory sake, we only have to store the previous row
        dp = [True] + [False]*half # always possible to make sum of 0 (don't pick anything)
        
        for i in range(len(nums)):
            next_dp = [True] + [False]*half
            for j in range(1, half+1):
                # at each sum, we can create the sum by using the new element or not
                # similar to knapsack
                not_using = dp[j]
                using = dp[j-nums[i]] if nums[i] <= j else False
                next_dp[j] = not_using or using
            dp = next_dp[:]

        return dp[-1]
```

- to see if the array can be divided into two equal subsets, we just need to make sure that a subset of the array can sum to half of the total sum of the array.
- to do this, we can do it either top-down or bottom-up with [[dynamic-programming]].
- when doing top-down, we can just use [[recursion]] with [[memoization]].
- with bottom-up, this problem is very similar to the knapsack problem.
	- at each value in `nums`, we can choose to either use it or not use it.
	- working up the possible `sum` values from 0 to half of the total sum, we know that the sum of `j` can be created using the numbers in `nums[:i]` with two cases: _(`dp[i][j]`, where `j` is the current sum)_
		- not using the current value `nums[i]`, we can just look at `dp[i-1][j]`.
		- using the current value, we look at `dp[i-1][j-nums[i]]` (only if `nums[i]` is $\leq j$.
	- for my actual implementation, i just store the previous row of the `dp` instead of everything, for memory purposes.

## References.

- https://en.wikipedia.org/wiki/Knapsack_problem

Categories:: [[dynamic-programming]], [[recursion]], [[memoization]]
