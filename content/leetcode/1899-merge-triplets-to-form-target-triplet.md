---
title: "1899. merge triplets to form target triplet"
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/merge-triplets-to-form-target-triplet/
tags:
  - greedy
  - array
date: 2023-01-16
updated: 2024-02-29
---

A **triplet** is an array of three integers. You are given a 2D integer array `triplets`, where `triplets[i] = [ai, bi, ci]` describes the `ith` **triplet**. You are also given an integer array `target = [x, y, z]` that describes the **triplet** you want to obtain.

To obtain `target`, you may apply the following operation on `triplets` **any number** of times (possibly **zero**):

- Choose two indices (**0-indexed**) `i` and `j` (`i != j`) and **update** `triplets[j]` to become `[max(ai, aj), max(bi, bj), max(ci, cj)]`.
    - For example, if `triplets[i] = [2, 5, 3]` and `triplets[j] = [1, 7, 5]`, `triplets[j]` will be updated to `[max(2, 1), max(5, 7), max(3, 5)] = [2, 7, 5]`.

Return `true` _if it is possible to obtain the_ `target` _**triplet**_ `[x, y, z]` _as an **element** of_ `triplets`_, or_ `false` _otherwise_.

## solution

We note that if a triplet has a value that’s too big for `target`, we can’t do any operations with it because we’ll overshoot the value in `target`.

If there’s a triplet that has a value that matches the value in target, then we know we can use it along with some other value that doesn’t violate the point mentioned above.

```python
class Solution:
	def mergeTriplets(self, triplets: List[List[int]], target: List[int]) -> bool:
		tx, ty, tz = target
		acc = [0, 0, 0]

		for x, y, z in triplets:
			if [x,y,z] == target:
				return True

			if x <= tx and y <= ty and z <= tz:
				acc = [max(i, j) for i, j in zip(acc, [x,y,z])]

return acc == target
```
