# 278. First Bad Version

```python
class Solution:
    def firstBadVersion(self, n: int) -> int:
        l, r = 1, n
        
        while True:
            m = (l+r)//2
            
            if isBadVersion(m) and not isBadVersion(m-1):
                return m
            elif isBadVersion(m) and isBadVersion(m-1):
                r = m - 1
            else:
                l = m + 1
```

- just a simple [[binary-search]].