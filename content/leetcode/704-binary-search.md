---
title: 704. binary search
date: 2022-11-11
updated: 2024-02-29
tags:
  - binary-search
---

Let’s start from this template that matches the functionality of `bisect_left`.

It returns the index of the first occurrence of an element if it exists, and the correct insertion index if the element doesn’t exist.

```python
def search(self, nums: List[int], target: int) -> int:
	l,r = 0, len(nums)-1

	while l < r:
		m = (l+r) // 2

		if nums[m] < target:
			l = m+1
		else:
			r = m

return l if nums[l] == target else -1
```

Then, to adapt this `bisect_left` function to our use case, just check if the index returned contains our target, else return -1.
