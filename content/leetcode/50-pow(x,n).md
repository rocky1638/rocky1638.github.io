---
created_at: 2022-12-29
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/powx-n/
---

# 50. Pow(x, n)

```python
class Solution:
    def myPow(self, x: float, n: int) -> float:
        if n == 0: return 1
        if n < 0:
            n = abs(n)
            x = 1/x

        memo = {}
        def recurse(val, exp):
            if exp == 1:
                return val
            
            first_half = exp // 2
            second_half = exp - first_half

            if first_half in memo: val1 = memo[first_half] 
            else:
                val1 = recurse(val, first_half)
                memo[first_half] = val1

            if second_half in memo: val2 = memo[second_half] 
            else:
                val2 = recurse(val, second_half)
                memo[second_half] = val2

            return val1 * val2

        return recurse(x, n)
```

- i first tried to do it linearly by just multiplying $x$ repeatedly by itself, but that was too slow.
- then, i realized that you can [[divide-and-conquer]] by splitting the exponent in half each time and using [[recursion]].
- this still timed out, so i realized that there were many computations that were being repeated, so decided to use [[memoization]] to speed up the process significantly.

Categories:: [[divide-and-conquer]], [[recursion]], [[memoization]]
