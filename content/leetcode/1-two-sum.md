---
created: 2022-12-02
type: leetcode
difficulty: 🟢
link: https://leetcode.com/problems/two-sum/
---

# 1. Two Sum

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        d = {}
        for i, num in enumerate(nums):
            if num in d:
                return [d[num], i]
            
            d[target-num] = i
```

- use a [[hashmap]] to store the numbers we’ve seen so far.

Categories:: [[array]], [[hashmap]]
