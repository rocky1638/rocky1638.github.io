---
type: leetcode
title: 239. sliding window maximum
aliases: 
difficulty: 🔴
link: https://leetcode.com/problems/sliding-window-maximum/
date: 2023-01-06
updated: 2024-03-19
tags:
  - sliding-window
  - heap
---

You are given an array of integers nums, there is a sliding window of size `k` which is moving from the very left of the array to the very right. You can only see the `k` numbers in the window. Each time the sliding window moves right by one position.

Return the array of max values in each sliding window across the array.

## solutions

### heap

Two versions of the heap solution that I wrote at different times are below.

```python
class Solution:
    def maxSlidingWindow(self, nums: List[int], k: int) -> List[int]:
        """
        - we can use a max heap to keep track of the largest value in the current window.
        - how do we update values in the heap as we slide our window?
            -  maybe "lazy" delete the values in the heap?
            - i.e. store the index of the values in the heap as well.
                - when we go to look for max, if the value at the top is already outside of the window, pop it and keep looking down.
        """
        ans = []
        
        # create heap and check max of first window
        h = []
        for i, num in enumerate(nums[:k]):
            heapq.heappush(h, (-num, i))
        ans.append(-h[0][0])
        
        # the rest of the windows
        for i in range(k, len(nums)):
            num = nums[i]
            # append new value in this window
            heapq.heappush(h, (-num, i))

            # keep popping until max value is in the window
            while h[0][1] <= (i-k):
                heapq.heappop(h)   

            # max in heap should now be in window
            ans.append(-h[0][0])
        
        return ans
```

```python
def maxSlidingWindow(self, nums: List[int], k: int) -> List[int]:
	ans = []
	# heap[i] = (-val, idx)
	max_heap = []
	# add first k elements to heap
	for i in range(k):
		heappush(max_heap, (-nums[i], i))
		l, r = 0, k-1
		while True:
			# remove values that are no longer in our window 
			while max_heap and max_heap[0][1] < l:
				heappop(max_heap)
				ans.append(-max_heap[0][0])
				l += 1
				r += 1
				if r < len(nums):
					# add next value on right side of # sliding window to the heap
					heappush(max_heap, (-nums[r], r))
				else:
					break
	return ans
```

### double-ended queue

By using a double-ended queue and greedily removing elements from the queue, we can achieve amortized $O(2n)$ time which is asymptotically $O(n)$. This is because each element is only ever added once and removed once.

The key insight is that when maintaining our double-ended queue of window values, we can greedily pop all the prior values in the queue that are smaller than the one we’re adding before adding our new value.

This, along with first pruning values at the front of the queue that are no longer in our window range, allows us to guarantee that the first element of the queue will be the largest value in our window (it has to be… if it wasn’t, the new value would have knocked it out — or it is the new value that we just added).

```python
def maxSlidingWindow(self, nums: List[int], k: int) -> List[int]:
	ans = []
	dq = deque()
	  
	for i in range(len(nums)):
		# pop values that are no
		# longer in the window
		while dq and dq[0] <= i-k:
			dq.popleft()

		# pop values that are smaller
		# then nums[i], before we add nums[i]
		while dq and nums[dq[-1]] < nums[i]:
			dq.pop()
		  
		dq.append(i)

		if i >= k-1:
			ans.append(nums[dq[0]])

	return ans
```
