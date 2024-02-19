---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/time-based-key-value-store/
---

# 981. Time Based Key-Value Store

```python
class TimeMap:
    def __init__(self):
        self.d = defaultdict(list)

    def set(self, key: str, value: str, timestamp: int) -> None:
        self.d[key].append((timestamp, value))

    def get(self, key: str, timestamp: int) -> str:
        # binary search for most recent timestamp <= requested timestamp
        a = self.d[key]
        l, r = 0, len(a)-1
        
        while l <= r:
            m = (l+r)//2
            
            # found the exact timestamp
            if a[m][0] == timestamp:
                return a[m][1]
            
            # if current timestamp is in the future
            # compared to the requested one
            elif a[m][0] > timestamp:
                r = m - 1
                
            # we found the most recent one that occurred before
            # the requested timestamp
            elif (m+1)==len(a) or a[m+1][0] > timestamp:
                return a[m][1]
            
            # only other case is to look to the right
            else:
                l = m + 1
        return ""
```

- we use a [[hashmap]] to store values of every `key`.
- at each index of the hashmap, we keep a sorted [[array]] of `timestamp` and `value`.
- because these arrays are sorted, when we search for timestamps in `get`, we can use [[binary-search]].

Categories:: [[binary-search]], [[hashmap]], [[array]]
