---
created_at: 2023-01-11
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/combination-sum-ii/
---

# 40. Combination Sum II

Given a collection of candidate numbers (`candidates`) and a target number (`target`), find all unique combinations in `candidates` where the candidate numbers sum to `target`.

Each number in `candidates` may only be used **once** in the combination.

**Note:** The solution set must not contain duplicate combinations.

```python
class Solution:
    def combinationSum2(self, candidates: List[int], target: int) -> List[List[int]]:
        seen = set()
        ans = []
        nums = sorted(candidates)

        blocks = []
        cur = None 
        for num in nums:
            if cur is None:
                cur = num
                count = 1
            elif cur == num:
                count += 1
            else:
                blocks.append((cur, count))
                cur = num
                count = 1
        blocks.append((cur, count)) 
        
        def backtrack(tally, acc, idx):
            nonlocal seen

            if tally == target: ans.append(acc)
            elif idx >= len(blocks): return

            else:
                # we take anywhere from 0 to n of the block
                val, cnt = blocks[idx]
                for amt in range(cnt+1):
                    new_tally = tally + amt * val
                    if new_tally <= target:
                        backtrack(new_tally, acc[:]+amt*[val], idx+1)
            
        backtrack(0, [], 0)
        return ans
```

- we use a similar block representation that we used in [[39-combination-sum]] after sorting the array.
- then, we use backtracking to choose a number between $[0,k]$ to pick of a certain block of the same numbers to include in our `acc` for the next recursion.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[39-combination-sum]]

## References.

Categories:: [[backtracking]], [[recursion]], [[sorting]], [[array]]
