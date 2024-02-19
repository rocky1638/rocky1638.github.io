# 1387. Sort Integers by the Power Value

```python
class Solution:
    def getKth(self, lo: int, hi: int, k: int) -> int:
        memo = {}
        
        def calcPowerValue(num):
            steps = 0
            cur = num
            
            while True:
                # if we've reached 1, memoize it and return the steps counter
                if cur == 1:
                    memo[num] = steps
                    return steps
                # stop early if we've calculated this intermediate step before
                elif cur in memo:
                    steps += memo[cur]
                    memo[num] = steps
                    return steps
                else:
                    if cur % 2 == 0:
                        cur = cur // 2
                    else:
                        cur = 3 * cur + 1
                    steps += 1
        
        a = []
        for num in range(lo, hi+1):
            power = calcPowerValue(num)
            a.append((num, power))
            
        a.sort(key=lambda x: (x[1], x[0]))
        return a[k-1][0]
```

- key realization is that when we calculate power values for a bunch of numbers, we will encounter a bunch of repeated calculations!
- so, we should use [[memoization]].
- now with memoization, just iterate through and calculate all the power values.
- at the end, use [[sorting]] to find the correct answer.