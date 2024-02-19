---
created_at: 2023-01-04
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/binary-search/
---

# 704. Binary Search

```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        l, r = 0, len(nums) - 1

        while l <= r:
            m = (l+r)//2

            if nums[m] == target:
                return m
            elif nums[m] < target:
                l = m + 1
            else:
                r = m - 1

        return -1
```

- literally just [[binary-search]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[binary-search]], [[array]]
