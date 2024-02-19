---
created_at: 2022-12-20
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/single-number/
---

# 136. Single Number

```python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        ans = nums[0]
        for num in nums[1:]:
            # XOR returns 0 when doing two of the same number
            ans ^= num
        return ans
```

- we use a logical xor between each of the integers, because two identical numbers, when xor’d will give 0.
- only the bits for the single number will remain.

Categories:: [[math]], [[array]]
