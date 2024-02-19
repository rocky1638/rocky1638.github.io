---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/combination-sum/
---

# 39. Combination Sum

Given an array of **distinct** integers `candidates` and a target integer `target`, return _a list of all **unique combinations** of_ `candidates` _where the chosen numbers sum to_ `target`_._ You may return the combinations in **any order**.

The **same** number may be chosen from `candidates` an **unlimited number of times**. Two combinations are unique if the frequency of at least one of the chosen numbers is different.

The test cases are generated such that the number of unique combinations that sum up to `target` is less than `150` combinations for the given input.

```python
class Solution:
    def combinationSum(self, candidates: List[int], target: int) -> List[List[int]]:
        seen = set()
        ans = []
        
        def backtrack(tally, acc, cand_idx):
            key = f"{tally}{str(acc)}"
            if key in seen:
                return
            
            if tally == target:
                ans.append(acc)
            
            elif tally > target:
                return
            
            else:
                for i in range(cand_idx, len(candidates)):
                    cand = candidates[i]
                    newkey = f"{tally}{str(acc+[cand])}"
                    backtrack(tally + cand, acc[:]+[cand], i)
                    seen.add(newkey)
            
        backtrack(0, [], 0)
        return ans
```

- classic [[backtracking]], where we try to assemble valid combinations from the top-down.
- with each recursive call, we go through the list of candidates in order, either choosing to append the current candidate again, or to append the next candidate.
	- if our tally ever equals the target, we take the valid combination and append it to `ans`.
	- else, if our tally is past the target, we can just stop that branch of the backtracking.

Categories:: [[backtracking]], [[recursion]]
