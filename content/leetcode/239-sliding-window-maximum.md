---
created_at: 2023-01-06
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/sliding-window-maximum/
---

# 239. Sliding Window Maximum

You are given an array of integers nums, there is a sliding window of size `k` which is moving from the very left of the array to the very right. You can only see the `k` numbers in the window. Each time the sliding window moves right by one position.

Return the array of max values in each sliding window across the array.

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

- see the comments for a description.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[heap]], [[array]]
