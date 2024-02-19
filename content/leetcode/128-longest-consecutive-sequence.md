---
created_at: 2022-12-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/longest-consecutive-sequence/
---

# 128. Longest Consecutive Sequence

```python
class Solution:
    def longestConsecutive(self, nums: List[int]) -> int:
        if not nums:
            return 0
            
        ans = 1
        s = set(nums)

        for num in nums:
            # if the lower number is in nums, we wanna start with that one
            if num-1 not in s:
                cur = num
                count = 1
                while cur+1 in s:
                   cur += 1
                   count += 1 
                   ans = max(ans, count)
        return ans
```

- the brute force method is for each number, to continually see if the next number appears in the [[array]].
- the crux of the issue is to check array membership in linear time, for which we can use a set.
- then, for each number, if it is the smallest number in a sequence *(which we can check by seeing if the number one less than it is in the array)*, we iterate as long as the next number is also in the set.
	- keep a running tally to store our best answer and then return it.

Categories:: [[array]], [[hashmap]]
