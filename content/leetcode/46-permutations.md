---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/permutations/
---

# 46. Permutations

Given an array `nums` of distinct integers, return _all the possible permutations_. You can return the answer in **any order**.

```python
class Solution:
    def permute(self, nums: List[int]) -> List[List[int]]:
        seen = set()
        acc = []
        ans = []
        
        def backtrack():
            if len(acc) == len(nums):
                ans.append(acc[:])
            else:
                for num in nums:
                    if num not in seen:
                        seen.add(num)
                        acc.append(num)
                        
                        backtrack()
                        
                        acc.pop()
                        seen.remove(num)
        
        backtrack()
        return ans
```

- classic [[backtracking]].
- don’t actually have to pass accumulator and seen sets in the function call. We can just add to it before we call `backtrack()` and reset it after returning from the call.

Categories:: [[array]], [[backtracking]]
