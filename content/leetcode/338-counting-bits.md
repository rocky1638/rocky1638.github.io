# 338. Counting Bits

```python
class Solution:
    def countBits(self, n: int) -> List[int]:
        a = [0]*(n+1)
        for i in range(1, n+1):
            if i % 2 == 0:
                a[i] = a[i//2]
            else:
                a[i] = a[i//2]+1
        return a
```

- we know by [[math]] that any even number $i$ will have the same number of one bits as the number $i / 2$.
- also know that the odd number $i$ will have one more bit than the number $i/2$.
- i have no idea why this works to be honest.