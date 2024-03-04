---
type: leetcode
title: 1143. longest common subsequence
difficulty: 🟡
tags:
  - dp
aliases: 
parents: 
children: 
supports: 
enemies: 
date: 2022-12-30
updated: 2024-03-04
---

Given two strings `text1` and `text2`, return _the length of their longest **common subsequence**._ If there is no **common subsequence**, return `0`.

A **subsequence** of a string is a new string generated from the original string with some characters (can be none) deleted without changing the relative order of the remaining characters.

- For example, `"ace"` is a subsequence of `"abcde"`.

A **common subsequence** of two strings is a subsequence that is common to both strings.

## solutions

We keep pointers for both strings `text1` and `text2`. When the two characters `text1[i]` and `text2[j]` are equal, we know that our longest common subsequence will be the answer we had for `text1[:i-1]` and `text2[j-1]`.

Otherwise, we can’t make a match with the two current characters, so we essentially take our best score from our previous combinations. This is either `text1[i-1], text2[j]` or `text1[i], text2[j-1]`.

With this intuition, we can do backtracking with memoization, or use a `dp` array.

> [!help]- More intuition details
> When we're iterating through the two strings with two pointers and two values don't match, we **must** skip one of the characters.
>
> Think about if you solved this by hand. Every time the two characters at your pointers aren’t matching, you have to decide to move one of them forward to try to match against the pointer at the other string!
>
> This is why we take the maximum of `dp[i-1][j]` and `dp[i][j-1]`. Each of those prior values indicate choosing to skip a value in `text1` or a value in `text2`.

### backtracking w/ memoization

```python
def longestCommonSubsequence(self, text1: str, text2: str) -> int:

	@lru_cache(None)
	def helper(i,j):
		if i<0 or j<0:
			return 0
		if text1[i]==text2[j]:
			return helper(i-1,j-1)+1
		return max(helper(i-1,j),helper(i,j-1))

	return helper(len(text1)-1,len(text2)-1)
```

### 2d dynamic programming

```python
def longestCommonSubsequence(self, text1: str, text2: str) -> int:
	dp = [[0 for j in range(len(text2))] for i in range(len(text1))]
	
	for i in range(len(text1)):
		for j in range(len(text2)):
			val = 0
			if text1[i] == text2[j]:
				if i > 0 and j > 0:
					val = dp[i-1][j-1] + 1
				else:
					val = 1
			if i > 0:
				val = max(val, dp[i-1][j])
			if j > 0:
				val = max(val, dp[i][j-1])
			dp[i][j] = val
	return dp[-1][-1]
```
