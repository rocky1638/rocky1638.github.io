---
created_at: 2023-01-16
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/jump-game-ii/
---

# 45. Jump Game II

You are given a **0-indexed** array of integers `nums` of length `n`. You are initially positioned at `nums[0]`.

Each element `nums[i]` represents the maximum length of a forward jump from index `i`. In other words, if you are at `nums[i]`, you can jump to any `nums[i + j]` where:

- `0 <= j <= nums[i]` and
- `i + j < n`

Return _the minimum number of jumps to reach_ `nums[n - 1]`. The test cases are generated such that you can reach `nums[n - 1]`.

```python
class Solution:
    def jump(self, nums: List[int]) -> int:
        dp = [float("inf")]*len(nums)
        dp[-1] = 0

        for i in reversed(range(len(nums)-1)):
            for jump in range(i+1, min(len(nums), i+nums[i]+1)):
                if dp[jump] is not None:
                    dp[i] = min(dp[i], dp[jump]+1)
        return dp[0]
```

- we just keep track of the minimum number of jumps is required to reach the end from index $i$ in `dp[i]`.
	- our base case is 0 in the final index of the `dp` array.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[55-jump-game]].

## References.

Categories:: [[dynamic-programming]], [[array]]
