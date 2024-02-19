---
created_at: 2022-12-10
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/maximum-product-subarray/
---

# 152. Maximum Product Subarray

```python
class Solution:
    def maxProduct(self, nums: List[int]) -> int:
        if len(nums) == 0:
            return 0

        ans = nums[0]

        # dp[i] = (biggest product ending here, smallest product ending here)
        dp = [(nums[0], nums[0])]
        for i in range(1, len(nums)):
            val = nums[i]
            a, b = val * dp[-1][0], val * dp[-1][1]
            ans = max(ans, a, b, val)
            dp.append((max(a, b, val), min(a, b, val)))
        return ans
```

- we use [[dynamic-programming]] to store the maximum and minimum subarray products that end at the current index.
- we need to store maximum and minimum because if we see a new negative number, we have to multiply by another negative number to possible get our biggest positive number.

Categories:: [[array]], [[dynamic-programming]]
