---
created_at: 2022-11-11
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
---

# 121. Best Time to Buy and Sell Stock

```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        lowestsofar = float("inf")
        ans = 0
        
        for num in prices:
            ans = max(ans, num-lowestsofar)
            lowestsofar = min(lowestsofar, num)
        
        return ans
```

- iterate through the [[array]] and keep track of the lowest one so far, and the best profit so far.

Categories:: [[array]], [[two-pointers]]
