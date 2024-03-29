---
title: 42. trapping rainwater
type: leetcode
aliases: 
difficulty: 🔴
link: https://leetcode.com/problems/trapping-rain-water/
date: 2022-11-24
updated: 2024-03-14
tags:
  - two-pointer
  - array
---

Given `n` non-negative integers representing an elevation map where the width of each bar is `1`, compute how much water it can trap after raining.

## solutions

### two iterations

The brute force way to approach this is to iterate through the heights, and for each height, we go outwards with two pointers towards the edges of the structure to find the tallest enclosing walls on each side.

We can improve on this by memoizing the tallest wall to the left and right of each index. Furthermore, we only really need to store one of them, because the other direction can be stored in a single value as we iterate.

```python
def trap(self, height: List[int]) -> int:
	maxtoleft = 0
	maxtoright = [0]
	ans = 0
	
	# create maxtoright array
	for h in reversed(height[1:]):
		maxtoright.append(max(h, maxtoright[-1]))
		maxtoright = maxtoright[::-1]
	
	# iterate from left
	for i in range(len(height)):
		minwall = min(maxtoleft, maxtoright[i])
		if height[i] < minwall:
			ans += minwall - height[i]
		maxtoleft = max(maxtoleft, height[i])
	return ans
```

### one iteration

We can actually improve further to only one iteration by using [[two-pointers]] going inwards from the edges, and keep track of both max from left and max from right in two single values.

The key insight is that the amount of water stored at index `i` is only dependent on the smaller of the two maximum walls!

For example, if we are at an index where we know that the left maximum wall is shorter than the right maximum wall so far, we can safely use the height of left maximum wall to calculate the amount of water stored, and *don’t actually care about the rest of the walls to the right that we haven’t checked yet.*

This is because in both cases, our answer stays the same:

- If there’s a wall to the right that we haven’t seen yet that is taller than `rightmax`, it doesn’t matter because our water stored is still dependent on the current `leftmax`.
- If there’s a wall to the right that we haven’t seen yet that is shorter than `rightmax`, it’s irrelevant because `rightmax` is already bigger.

```python
def trap(self, height: List[int]) -> int:
	l, r = 0, len(height)-1
	leftmax, rightmax = 0, 0
	ans = 0
	
	while l < r:
		leftmax = max(leftmax, height[l])
		rightmax = max(rightmax, height[r])
		
		if leftmax < rightmax:
			ans += (max(0, leftmax-height[l]))
			l += 1
		else:
			ans += (max(0, rightmax-height[r]))
			r -= 1
	return ans
```
