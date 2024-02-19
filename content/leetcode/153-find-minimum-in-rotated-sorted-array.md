---
created_at: 2023-01-04
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/
---

# 153 Find Minimum In Rotated Sorted Array

```python
class Solution:
    def findMin(self, nums: List[int]) -> int:
        l, r = 0, len(nums)-1
            
        while l <= r:
            m = (l+r)//2
            
            if (m+1) < len(nums) and nums[m] > nums[m+1]:
                return nums[m+1]
            elif nums[m] < nums[0]: # we're in the right half
                r = m - 1
            else:
                l = m + 1
                
        # array is not rotated
        return nums[0]
```

- use binary search to find where the array is split.
- if the array is not rotated, return the first element.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[33-search-in-rotated-sorted-array]].
	- literally just the first half of this question.
- [[704-binary-search 1]].

## References.

Categories:: [[array]], [[binary-search]]
