---
title: 55. jump game
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/jump-game/
date: 2022-12-21
updated: 2024-02-25
tags:
  - dp
  - greedy
  - array
---
You are given an integer array `nums`. You are initially positioned at the array's **first index**, and each element in the array represents your maximum jump length at that position.

Return `true` _if you can reach the last index, or_ `false` _otherwise_.

## top-down recursion w/ memoization (tle).

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
        
	  return recurse(0)
```

- we use backtracking while also using memoization to store if an index can reach the end of the array.

## bottom-up dynamic programming.

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

- we use a `dp` array such that for any value $dp[i]$, the value is `True` if we can reach the end of the array from index $i$.
	- the key here is that we work backwards through the array, because our base case is that the value of the `dp` at the last index is equal to `True` _(and that is the only information we start with)_.
	- we build up from the right to the left to see if $dp[0]$ is `True`.
	- at every index, we scan to the right on the squares that we can jump to from the current index, and see if any of them allow us to continue to the end of the array.
		- if we find one, then we can set the value of $dp$ at that index to `True`.

## optimized $O(1)$ space bottom-up dynamic programming

```python
class Solution:
	def canJump(self, nums: List[int]) -> bool:
		closest_true = len(nums)-1

		for i in reversed(range(len(nums)-1)):
			if i+nums[i] >= closest_true:
				closest_true = i

		return closest_true == 0
```

- an observation from the above solution is that we don’t actually need to look at all of the possible places that we can jump from a certain step.
- all we need to know is if we can reach the lowest step that allows us to reach the top.
	- so, we just check if the jump range from our current step to see if it encompasses that step.
