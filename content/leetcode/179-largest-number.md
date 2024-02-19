---
created_at: 2022-12-31
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/largest-number/
---

# 179. Largest Number

```python
class Solution:
    def largestNumber(self, nums: List[int]) -> str:
        """
		- sort greedily.
		- if two adjacent numbers a + b form a bigger number as ab then ba, then
		  sort a in front of b.
        """

        def sortFunc(x1, x2):
            if x1+x2 > x2+x1:
                return 1
            elif x1+x2 < x2+x1:
                return -1
            return 0 

        nums = [str(x) for x in nums]
        nums.sort(key=functools.cmp_to_key(sortFunc), reverse=True)
        if nums[0] == "0":
            return "0"
        return "".join(nums)
```

- we use a [[greedy]] approach to [[sorting]] to try to get the optimal way to move the biggest digits to the most significant positions in the final number

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[array]], [[greedy]], [[sorting]]
