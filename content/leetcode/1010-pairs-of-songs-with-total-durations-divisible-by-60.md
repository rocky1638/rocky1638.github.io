# 1010. Pairs of Songs With Total Durations Divisible by 60

```python
class Solution:
    def numPairsDivisibleBy60(self, time: List[int]) -> int:
        mods = [0]*60
        ans = 0
        
        for t in time:
            mods[t%60] += 1
        
        # for when the numbers are already 0 mod 60
        ans += math.comb(mods[0], 2)
        
        l, r = 1, 59
        while l < r:
            ans += mods[l] * mods[r]
            l += 1
            r -= 1
        
        ans += math.comb(mods[30], 2)
        
        return ans
```

- we can reduce the complexity of looking at pairs when we realize that we only have to consider each value $t$ in `time` as its $\mod60$ counterpart.
- we can store the count of how many numbers are $x\mod60$ where $x$ is between 0 and 59.
- then, we can just use basic combinatorics math to figure out how many possible combinations there are.
	- have to use `math.comb` for the number of numbers that are mod 60 and mod 30.

[[math]], [[array]], [[hashmap]]