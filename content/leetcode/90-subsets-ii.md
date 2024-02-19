---
created_at: 2023-01-10
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/subsets-ii
---

# 90. Subsets II

## Using extra space.

```python
class Solution:
    def subsetsWithDup(self, nums: List[int]) -> List[List[int]]:
        ans = [[]]
        seen = set()
        nums.sort()
        
        def backtrack(idx, acc):
            if idx < len(nums):
                # don't take the current number
                backtrack(idx+1, acc)
                # take the current number
                backtrack(idx+1, acc[:]+[nums[idx]])

                new = "".join(map(str, acc[:]+[nums[idx]]))
                if new not in seen:
                    ans.append(acc[:]+[nums[idx]])
                    seen.add(new)
            
        backtrack(0, [])
        return ans
```

- we use a set here to remember the subsets that we’ve seen already.
- we sort because leetcode expects the actual subsets to be in order.

## Without extra space.

```python
class Solution:
    def subsetsWithDup(self, nums: List[int]) -> List[List[int]]:
        """
        - the only way we get duplicates are when there are multiples
          of the same number, and we can pick some of them.
        - if we sort the array, we can think of these duplicates as blocks.
        - then, in one recursive iteration, we can pick 0-n of these
          duplicates in a block and recurse.
        """

        ans = [[]]
        nums.sort()

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
        
        def backtrack(idx, acc):
            if idx < len(blocks):
                val, count = blocks[idx]
                for cnt in range(count+1):
                    # take the current number cnt times
                    backtrack(idx+1, acc[:]+cnt*[val])
                    if cnt > 0:
                        ans.append(acc[:]+cnt*[val])
            
        backtrack(0, [])
        return ans
```

- instead of keeping a set to store what we’ve seen, we just store the duplicates in “blocks”, and then we can recurse on every possible number of them at once instead of risking the chance of using the same number of a duplicate in two recursive branches.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[backtracking]], [[recursion]], [[array]], [[hashmap]]
