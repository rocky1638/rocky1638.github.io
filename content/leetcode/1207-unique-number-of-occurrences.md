# 1207. Unique Number of Occurrences

```python
class Solution:
    def uniqueOccurrences(self, arr: List[int]) -> bool:
        counts = collections.Counter()

        for num in arr:
            counts[num] += 1

        seen = set()
        for freq in counts.values():
            if freq in seen:
                return False
            seen.add(freq)
        return True
```

- create a [[frequency-map]] to see the counts of each number.
- check all the counts for uniqueness using a set.

[[array]], [[hashmap]]