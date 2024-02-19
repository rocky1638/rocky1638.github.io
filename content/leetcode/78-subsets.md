---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/subsets/
---

# 78. Subsets

Given an integer array `nums` of **unique** elements, return _all possible subsets (the power set)_.

The solution set **must not** contain duplicate subsets. Return the solution in **any order**.

```python
class Solution:
    def subsets(self, nums: List[int]) -> List[List[int]]:
        ans = [[]]
        
        def backtrack(idx, acc):
            if idx < len(nums):
                backtrack(idx+1, acc)
                backtrack(idx+1, acc[:]+[nums[idx]])
                ans.append(acc[:]+[nums[idx]])
            
        backtrack(0, [])
        return ans
```

- classic backtracking problem, at each [[recursion]], we decide to whether take the current value at `idx` or not.
- note that we only add the new subset to the `ans` array if we decide to take the current value, or else we will end up with a bunch of duplicates in the `ans` array.

Categories:: [[recursion]], [[backtracking]], [[array]]
