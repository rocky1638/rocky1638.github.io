---
created_at: 2023-01-18
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/relative-sort-array/
---

# 1122. Relative Sort Array

Given two arrays `arr1` and `arr2`, the elements of `arr2` are distinct, and all elements in `arr2` are also in `arr1`.

Sort the elements of `arr1` such that the relative ordering of items in `arr1` are the same as in `arr2`. Elements that do not appear in `arr2` should be placed at the end of `arr1` in **ascending** order.

```
Example:
Input: arr1 = [2,3,1,3,2,4,6,7,9,2,19], arr2 = [2,1,4,3,9,6]
Output: [2,2,2,1,4,3,3,9,6,7,19]
```

```python
class Solution:
    def relativeSortArray(self, arr1: List[int], arr2: List[int]) -> List[int]:
        ans = []
        c1 = collections.Counter(arr1)
        
        for num in arr2:
            while c1[num] > 0:
                ans.append(num)
                c1[num] -= 1
           
        for key in sorted(c1.keys()):
            for i in range(c1[key]):
                ans.append(key)
                
        return ans
```

- we keep a frequency counter for `arr1`, and just move all the values that match with a value in `arr2` into a new output array.
- then, just sort the rest of the values and append them to the output array.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[frequency-map]], [[hashmap]], [[array]], [[sorting]]
