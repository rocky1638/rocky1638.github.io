---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/target-sum/
---

# 494. Target Sum

You are given an integer array `nums` and an integer `target`.

You want to build an **expression** out of nums by adding one of the symbols `'+'` and `'-'` before each integer in nums and then concatenate all the integers.

- For example, if `nums = [2, 1]`, you can add a `'+'` before `2` and a `'-'` before `1` and concatenate them to build the expression `"+2-1"`.

Return the number of different **expressions** that you can build, which evaluates to `target`.

## Top-down recursion with memoization.

```python
class Solution:
    def findTargetSumWays(self, nums: List[int], target: int) -> int:
        memo = {}
        def recurse(idx, tally):
            if idx == len(nums):
                if tally == target:
                    return 1
                return 0
            if (idx, tally) in memo:
                return memo[(idx, tally)]
            
            memo[(idx, tally)] = recurse(idx+1, tally+nums[idx]) + recurse(idx+1, tally-nums[idx])
            return memo[(idx, tally)]

        return recurse(0, 0)
```

- we use backtracking with memoization to solve this.
- memoize by keying the function calls by the index that we’re on, as well as the current subtotal.

## Dynamic programming with hashmap.

```python
class Solution:
    def findTargetSumWays(self, nums: List[int], target: int) -> int:
        """
        - "dp" with a hashmap
            - each level i stores the number of ways to create
              subtotals with the first i values in nums.
        """
        dp = {nums[0]: 1, -nums[0]: 1}
        # edge case for first num being zero
        if nums[0] == 0:
            dp = {0: 2}
        for i in range(1, len(nums)):
            nextDP = {}
            # go through prev subtotals
            for prev_subtotal in dp:
                # we can either add or subtract new value
                add = prev_subtotal + nums[i]
                sub = prev_subtotal - nums[i]

                # update next row's dp
                if add in nextDP: nextDP[add] += dp[prev_subtotal]
                else: nextDP[add] = dp[prev_subtotal]
                if sub in nextDP: nextDP[sub] += dp[prev_subtotal]
                else: nextDP[sub] = dp[prev_subtotal]

            dp = nextDP

        return dp[target] if target in dp else 0
```

- instead of recursing, we can just store the frequency that each subtotal shows up for the previous right index of nums in a hashmap.
- create a new hashmap at every iteration.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[17-letter-combinations-of-a-phone-number]].
- [[935-knight-dialer]].

## References.

Categories:: [[dynamic-programming]], [[memoization]], [[recursion]], [[backtracking]]
