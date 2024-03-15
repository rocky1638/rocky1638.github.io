---
title: "97. interleaving string"
tags:
aliases: 
parents: 
children: 
supports: 
enemies:
date: 2022-12-30
updated: 2024-03-11
---

Given strings `s1`, `s2`, and `s3`, find whether `s3` is formed by an **interleaving** of `s1` and `s2`.

An **interleaving** of two strings `s` and `t` is a configuration where `s` and `t` are divided into `n` and `m`  substrings respectively, such that:

- `s = s1 + s2 + ... + sn`
- `t = t1 + t2 + ... + tm`
- `|n - m| <= 1`
- The **interleaving** is `s1 + t1 + s2 + t2 + s3 + t3 + ...` or `t1 + s1 + t2 + s2 + t3 + s3 + ...`

**Note:** `a + b` is the concatenation of strings `a` and `b`.

## solution

### recursion w/ memoization

```python
def isInterleave(self, s1: str, s2: str, s3: str) -> bool:
	if len(s1) + len(s2) != len(s3):
		return False
	
	memo = {}
	def recurse(idx1, idx2):
		if idx1 == len(s1) and idx2 == len(s2):
			return True
		if (idx1, idx2) in memo:
			return memo[(idx1, idx2)]
		
		ret = False
		if idx1 < len(s1) and s1[idx1] == s3[idx1+idx2]:
			ret = ret or recurse(idx1+1, idx2)
		
		if idx2 < len(s2) and s2[idx2] == s3[idx1+idx2]:
			ret = ret or recurse(idx1, idx2+1)

		memo[(idx1, idx2)] = ret
		return memo[(idx1, idx2)]

	return recurse(0, 0)
```

### 2d dynamic programming

This is a similar idea to recursion, but we build bottom-up. `dp[i][j]` represents whether we can build the first `i+j` letters in `s3` using the first `i` letters of `s2` and the first `j` letters of `s1`. (There’s an off-by-one calculation that needs to be done because we need to store base case rows/columns in the array that represent situations when we haven’t yet used any of either/both string(s)).

```python
def isInterleave(self, s1: str, s2: str, s3: str) -> bool:
	if len(s1) + len(s2) != len(s3):
		return False
	
	dp = [[0 for j in range(len(s1)+1)] for i in range(len(s2)+1)]
	
	for i in range(len(dp)):
		for j in range(len(dp[0])):
			if i == 0 and j == 0:
				dp[i][j] = True
			elif i == 0:
				dp[i][j] = s1[j-1] == s3[j-1] and dp[i][j-1]
			elif j == 0:
				dp[i][j] = s2[i-1] == s3[i-1] and dp[i-1][j]
	
			else:
				ret = False
	
				# we previously used all of the first j chars of s1,
				# so now we have to use i'th char of s2
				# to match the next char in s3
				if dp[i-1][j]:
					ret = ret or s2[i-1] == s3[i+j-1]

				# we previously used all of the first i chars of s2,
				# so now we have to use the j'th char of s1
				# to match the next char in s3
				if dp[i][j-1]:
					ret = ret or s1[j-1] == s3[i+j-1]

				dp[i][j] = ret
	
	return dp[-1][-1]
```
