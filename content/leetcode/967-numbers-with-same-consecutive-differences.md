# 967. Numbers With Same Consecutive Differences

```python
class Solution:
    def numsSameConsecDiff(self, n: int, k: int) -> List[int]:
        ans = []
        acc = []
        
        def backtrack():
            if len(acc) == n:
                ans.append("".join(acc))
            else:
                prev_dig = int(acc[-1])
                k_below = prev_dig - k
                k_above = prev_dig + k
                
                if k_below >= 0:
                    acc.append(f"{k_below}")
                    backtrack()
                    acc.pop()
                if k != 0 and k_above < 10:
                    acc.append(f"{k_above}")
                    backtrack()
                    acc.pop()
        
        for i in range(1, 10):
            acc.append(f"{i}")
            backtrack()
            acc.pop()
        
        return ans
```

- basic [[backtracking]] question with [[recursion]].
- small edge case for when $k=0$, we only recurse down one of the branches, because the two recursion branches are the same.