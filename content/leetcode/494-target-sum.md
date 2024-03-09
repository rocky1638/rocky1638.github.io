---
title: "494. target sum"
created_at: 2023-01-17
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/target-sum/
date: 2023-01-17
updated: 2024-03-09
tags:
  - dp
  - memoization
---

You are given an integer array `nums` and an integer `target`.

You want to build an **expression** out of nums by adding one of the symbols `'+'` and `'-'` before each integer in nums and then concatenate all the integers.

- For example, if `nums = [2, 1]`, you can add a `'+'` before `2` and a `'-'` before `1` and concatenate them to build the expression `"+2-1"`.

Return the number of different **expressions** that you can build, which evaluates to `target`.

## solution

### top-down recursion with memoization

This backtracking solution is pretty simple. We know that each step, we either add or subtract the current number to our sum, so we consider both possibilities, and recurse on the rest of the numbers in `nums`.

Without memoization, we have a $O(2^n)$ solution, where $n$ is the length of `nums`.

We can memoize on the recursion parameters, reducing our runtime to $O(2\sum{n}\cdot n) \equiv O(\sum{n} \cdot n)$, because the value of `acc` can be in the range of `[-sum(n), sum(n)]`, if we select all positives or negatives.

```python
def findTargetSumWays(self, nums: List[int], target: int) -> int:
	memo = {}

	def recurse(idx, acc):
		if idx == len(nums):
			return 1 if acc == target else 0
	
		if (idx, acc) in memo:
			return memo[(idx, acc)]
	
		ways = 0
		ways += recurse(idx+1, acc + nums[idx])
		ways += recurse(idx+1, acc - nums[idx])

		memo[(idx, acc)] = ways
		return memo[(idx, acc)]

	return recurse(0, 0)
```

### dynamic programming

With the intuition from above, it’s quite trivial to convert the memoization solution to dynamic programming. We just keep a 2D array and build up a bottom-up solution of figuring out how many ways we can create each sum in `[-sum(n), sum(n)]` using the first `i` elements in `nums`.

The recurrence relation, simplified, is `dp[i][j] = dp[i-1][j-nums[i]] + dp[i-1][j+nums[i]]`.


> [!tip]- A small technicality
> Because each row in the `dp` is indexed in the range $[0, 2\sum{n}+ 1]$, but we actually are representing the values in the range $[-\sum{n}, \sum{n}]$, we have to do a small transposition when doing the actual calculations in code.

```python
def findTargetSumWays(self, nums: List[int], target: int) -> int:
	su = sum(nums)
	
	if su < abs(target):
		return 0
	
	dp = [[0 for j in range(2 * su + 1)] for i in range(len(nums))]
	
	for i in range(len(dp)):
		for j in range(len(dp[0])):
			# we iterate from 0..2n-1, but we want to
			# do logic based on -n..n
			val = j - su
			if i == 0:
				if abs(val) == nums[0]:
					dp[i][j] = 2 if nums[0] == 0 else 1
			else:
				dp[i][val] = dp[i-1][val-nums[i]] + dp[i-1][val+nums[i]]
	
	return dp[i][target + su]
```

### dynamic programming with constant space

From the previous solution, we can see that we only ever use the previous row of the `dp`, so we can reduce our problem to an $O(1)$ space solution.

```python
def findTargetSumWays(self, nums: List[int], target: int) -> int:
	su = sum(nums)
	
	if su < abs(target):
		return 0
	
	prev_dp = [0 for j in range(2 * su + 1)]
	prev_dp[nums[0] + su] += 1
	prev_dp[su - nums[0]] += 1
	
	for i in range(1, len(nums)):
		next_dp = [0 for j in range(2 * su + 1)]
		for j in range(len(prev_dp)):
			val = j - su
			next_dp[val] = prev_dp[val-nums[i]] + prev_dp[val+nums[i]]
		prev_dp = next_dp
	
	return prev_dp[target + su]
```

## related

- [[17-letter-combinations-of-a-phone-number]].
- [[935-knight-dialer]].
