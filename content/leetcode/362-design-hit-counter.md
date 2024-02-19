# 362. Design Hit Counter

```python
class HitCounter:

    def __init__(self):
        # a[i] = (timestamp, prefix_sum)
        self.a = [(float("-inf"), 0)]
        self.sum = 0

    def hit(self, timestamp: int) -> None:
        self.sum += 1
        self.a.append((timestamp, self.sum))

    def getHits(self, timestamp: int) -> int:
        bottom_bound = bisect.bisect_right(self.a, timestamp-300, key=lambda x: x[0])
        return self.a[-1][1] - self.a[bottom_bound-1][1]
```

- the [[prefix-sum]] is kind of unnecessary.
	- we really only need to know the indices.
- because the total number of hits will be increasing because `getHits` will always be called in chronological order, we can [[binary-search]] on the array to find the cutoff where we should start considering hits *(in the past 300 seconds).*

[[array]]