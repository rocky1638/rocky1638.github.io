# 528. Random Pick with Weight

```python
class Solution:

    def __init__(self, w: List[int]):
        # in array, store upper bound of cumulative weight
        self.a = []

        tally = 0
        for weight in w:
            tally += weight
            self.a.append(tally)
        self.total = tally
        print(self.a)

    def pickIndex(self) -> int:
        target = self.total * random.random()
        # idx = bisect.bisect_left(self.a, target)
        l, r = 0, len(self.a)
        while l < r:
            m = (l+r)//2
            if target > self.a[m]:
                l = m + 1
            else:
                r = m
        return l
```

- we store the upper bounds of each index’s weight range in the [[array]], in a similar idea to [[prefix-sum]].
- then, we can generate a random number in the range of the total weight of the array, and find the “weight bucket” that the number fits into.
	- we can find this index by doing [[binary-search]].
		 - binary search for the largest number that is smaller than `target`.