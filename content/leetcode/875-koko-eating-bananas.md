---
created_at: 2023-01-04
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/koko-eating-bananas/
---

# 875. Koko Eating Bananas

Koko loves to eat bananas. There are `n` piles of bananas, the `ith` pile has `piles[i]` bananas. The guards have gone and will come back in `h` hours.

Koko can decide her bananas-per-hour eating speed of `k`. Each hour, she chooses some pile of bananas and eats `k` bananas from that pile. If the pile has less than `k` bananas, she eats all of them instead and will not eat any more bananas during this hour.

Koko likes to eat slowly but still wants to finish eating all the bananas before the guards return.

Return _the minimum integer_ `k` _such that she can eat all the bananas within_ `h` _hours_.

```python
class Solution:
    def minEatingSpeed(self, piles: List[int], h: int) -> int:
        l, r = 1, max(piles)
        best = float("inf")

        while l <= r: 
            k = (l + r) // 2
            time_to_eat = sum(math.ceil(x/k) for x in piles) 

            if time_to_eat <= h:
                best = min(best, k)
                # try to go lower?
                r = k - 1
            elif time_to_eat > h:
                l = k + 1
        
        return best
```

- we use binary search on the possible eating rates `k`, starting our bounds at 1 and the maximum sized pile of bananas.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[binary-search]], [[array]]
