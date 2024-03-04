---
title: 763. partition labels
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/partition-labels/
date: 2023-01-17
updated: 2024-03-01
tags:
  - greedy
  - hashmap
  - sliding-window
---

You are given a string `s`. We want to partition the string into as many parts as possible so that each letter appears in at most one part.

Note that the partition is done so that after concatenating all the parts in order, the resultant string should be `s`.

Return _a list of integers representing the size of these parts_.

## solution

This solution is a combination of a sliding window as well as a greedy approach.

We first note that if our window contains a character `c`, our partition will be, at minimum, ending at the last occurrence of `c` (not considering any other characters that we might pick up between now and then).

So, we first construct a hashmap of the index of the last occurrence of each character, and then maintain a sliding window, expanding our valid ending point `current_end` as necessary every iteration.

When we reach the valid ending spot `current_end` with our current index `r`, we know this partition is now valid, and append the length of the partition to the `ans` array.

```python
def partitionLabels(self, s: str) -> List[int]:
	last_occurrence = {}

	for i in reversed(range(len(s))):
		if s[i] not in last_occurrence:
			last_occurrence[s[i]] = i

	ans = []
	start = 0
	current_end = last_occurrence[s[0]]

	for r in range(len(s)):
		current_end = max(current_end, last_occurrence[s[r]])

		if r == current_end:
			ans.append(r-start+1)
			current_end += 1
			start = current_end
		  
	return ans
```
