---
created_at: 2022-12-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/jump-game/
---

# 55. Jump Game

## Top-down recursion w/ memoization (TLE).

```python
class Solution:
    def canJump(self, nums: List[int]) -> bool:
        memo = [None]*len(nums)
        def recurse(idx):
            if idx == len(nums)-1:
                return True
            
            if memo[idx] is not None:
                return memo[idx]

            ret = False
            for next_idx in range(idx+1, min(len(nums), idx+nums[idx]+1)):
                ret = ret or recurse(next_idx)
            return ret
        
        return recurse(0
```

- we use [[backtracking]] while also using [[memoization]] to store if an index can reach the end of the [[array]].

## Bottom-up dynamic programming.

```python
class Solution:
    def canJump(self, nums: List[int]) -> bool:
        # dp[i] is True if we can reach the end from index i
        dp = [False]*len(nums)
        dp[-1] = True

        # iterate backwards through nums
        for i in reversed(range(len(nums)-1)):
            for jump in range(i+1, min(len(nums), i+nums[i]+1)):
                if dp[jump]:
                    dp[i] = True
                    break

        return dp[0]
```

- we use a `dp` array that for any value $dp[i]$, the value is `True` if we can reach the end of the array from index $i$.
	- the key here is that we work backwards through the array, because our base case is that the value of the `dp` at the last index is equal to `True` *(and that is the only information we start with)*.
	- we build up from the right to the left to see if $dp[0]$ is `True`.
	- at every index, we scan to the right on the squares that we can jump to from the current index, and see if any of them allow us to continue to the end of the array.
		- if we find one, then we can set the value of $dp$ at that index to `True`.

Categories:: [[array]], [[backtracking]], [[memoization]], [[dynamic-programming]]
