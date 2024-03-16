---
title: 4. median of two sorted arrays
type: leetcode
aliases: 
difficulty: 🔴
link: https://leetcode.com/problems/median-of-two-sorted-arrays/
date: 2023-01-02
updated: 2024-03-16
tags:
  - binary-search
  - array
---

Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return **the median** of the two sorted arrays.

The overall run time complexity should be `O(log (m+n))`.

## solutions

### merge arrays — $O(n)$

This one’s very intuitive. Just merge the two sorted arrays into one sorted array, and then return the median.

```python
class Solution:
	def merge(self, a1, a2):
		i, j = 0, 0
		ret = []
		while i < len(a1) or j < len(a2):
			if i == len(a1):
				ret.append(a2[j])
				j += 1
			elif j == len(a2):
				ret.append(a1[i])
				i += 1
			else:
				if a1[i] < a2[j]:
					ret.append(a1[i])
					i += 1
				else:
					ret.append(a2[j])
					j += 1
		return ret
	  
	def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
	"""
	- merge array, then grab middle one/two elements for median
	"""
	  
	merged = self.merge(nums1, nums2)
	n = len(merged)
	  
	if n % 2 == 0:
		return (merged[n//2-1] + merged[n//2]) / 2
	return merged[n//2]
```

### split binary search — $O(\log(m+n))$

This solution is not very intuitive and pretty hard to reason about.

What we do is try to find a way to partition/binary search these two arrays without actually merging them.

We know if we can partition these two arrays as if they were one array into two equal sized partitions of length `(len(nums1) + len(nums2)) // 2`, then the values near the middle (minimum of right partition or maximum of left partition) are the central values.

```python
def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
	a, b = nums1, nums2
	total = len(a) + len(b)
	half = total // 2
	
	# a is always the shorter array
	if len(b) < len(a):
		a, b = b, a
	
	l, r = 0, len(a) - 1
	while True:
		ma = (l+r) // 2 # middle index for a
		mb = half - ma - 2 # middle index for b
		
		aleft = a[ma] if ma >= 0 else float("-infinity")
		aright = a[ma+1] if ma+1 < len(a) else float("infinity")
		bleft = b[mb] if mb >= 0 else float("-infinity")
		bright = b[mb+1] if mb+1 < len(b) else float("infinity")
		
		# partition is correct
		if aleft <= bright and bleft <= aright:
			if total % 2 == 0:
				return (max(aleft, bleft) + min(aright, bright)) / 2
			else:
				return min(aright, bright)
		
		elif aleft > bright:
			r = ma - 1
		else: # aright < bleft
			l = ma + 1
```

## Neetcode video notes.

- [02:32](https://www.youtube.com/watch?v=q6IEA26hvXc#t=152.54057795422364) the actual logical definition of a median.
- [03:16](https://www.youtube.com/watch?v=q6IEA26hvXc#t=196.84639202098083) we essentially want to simulate looking through a merged array without actually merging them.
	- we want to partition the array into valid left and right halfs, because then the median will just be in the middle.
- [08:27](https://www.youtube.com/watch?v=q6IEA26hvXc#t=507.3298399103546) how to partition into left and right partitions without merging.
- [10:34](https://www.youtube.com/watch?v=q6IEA26hvXc#t=634.1080160095368) once we partition one of the arrays, we know the size that the partition should be in the other array because the total size of the partition should be `(len(a)+len(b)) // 2`.
- [13:14](https://www.youtube.com/watch?v=q6IEA26hvXc#t=794.7069969904633) edge cases for when we don’t include either of the arrays in our partition.
- [14:08](https://www.youtube.com/watch?v=q6IEA26hvXc#t=848.4556927108475) code walkthrough.

## references

- https://www.youtube.com/watch?v=q6IEA26hvXc
