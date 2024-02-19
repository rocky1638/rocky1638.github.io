---
created_at: 2022-12-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/longest-increasing-subsequence/
---

# 300. Longest Increasing Subsequence

Given an integer array `nums`, return _the length of the longest **strictly increasing subsequence**_.

## Obvious [[dynamic-programming]] solution.

```python
class Solution:
    def lengthOfLIS(self, nums: List[int]) -> int:
        dp = [1] * len(nums)
        for i in range(1, len(nums)):
            for j in range(i):
                if nums[i] > nums[j]:
                    dp[i] = max(dp[i], dp[j] + 1)

        return max(dp)
```

- create an array `dp` of length `nums` to store the longest subsequence ending at $i$ at $dp[i]$.
- at each index, we iterate through the entirety of `dp`, and if we see a number that’s less than the current number at index $j$, we set `dp[i]` to `dp[j]+1`.
- this takes $O(n^2)$.

## Creating optimal subsequence in order.

```python
class Solution:
    def lengthOfLIS(self, nums: List[int]) -> int:
        sub = []
        for num in nums:
            i = bisect_left(sub, num)

            # If num is greater than any element in sub
            if i == len(sub):
                sub.append(num)
            
            # Otherwise, replace the first element in
            # sub greater than or equal to num
            else:
                sub[i] = num
        
        return len(sub)
```

- we try to create the optimal subsequence by keeping track of a increasing subsequence in `sub`.
	- if the next number we see is greater than the entire sequence, we append it to the end of the sequence.
	- else, we replace the first number bigger than the current number in the subsequence with the current number.
		- this is because we’re trying to optimize the subsequence to be as “small” as possible.
	- in the end, the optimal subsequence is in `sub`.

```python
# input
nums = [10,9,2,5,3,7,101,18]
# example sub
[10]
[9]
[2]
[2, 5]
[2, 3]
[2, 3, 7]
[2, 3, 7, 101]
[2, 3, 7, 18]
```

Categories:: [[array]], [[dynamic-programming]]
