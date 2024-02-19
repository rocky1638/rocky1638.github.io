---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/search-in-rotated-sorted-array/
---

# 33. Search in Rotated Sorted Array

```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        # [4,5,6,1,2,3]
        # pivot is 6
        def findPivot():
            l, r = 0, len(nums)-1
            
            while l <= r:
                m = (l+r)//2
                
                if (m+1) < len(nums) and nums[m] > nums[m+1]:
                    return m
                elif nums[m] < nums[0]: # we're in the right half
                    r = m - 1
                else:
                    l = m + 1
                    
            # array is not rotated
            return -1
        
        def binsearch(l, r):
            while l <= r:
                m = (l+r)//2
                
                if nums[m] == target:
                    return m
                elif nums[m] < target:
                    l = m + 1
                else:
                    r = m - 1
            return -1
        
        pivot = findPivot()
        
        if pivot == -1:
            return binsearch(0, len(nums)-1)
        else:
            if target >= nums[0]:
                # search in left half
                return binsearch(0, pivot)
            else:
                # search in right half
                return binsearch(pivot+1, len(nums)-1)
```

- first [[binary-search]] to find the pivot index.
- then [[binary-search]] on the correct side of the pivoted array *(rotated array is essentially two distinct sorted arrays).*

Categories:: [[array]], [[binary-search]]
