# 869. Reordered Power of Two

```python
class Solution:
    def reorderedPowerOf2(self, n: int) -> bool:
        powers_of_two = collections.defaultdict()
        powers_of_two[1] = collections.Counter("1")

        val = 1
        while val <= 10 ** 9:
            val *= 2
            powers_of_two[val] = collections.Counter(str(val))
        
        c = collections.Counter(str(n))
        for k in powers_of_two:
            print(powers_of_two[k])
            if c == powers_of_two[k]:
                return True
        return False
```

- there aren’t actually that many powers of two under $10^9$, so we can just enumerate all of them.
- we store all of the [[frequency-map]] for each of these powers of two in a [[hashmap]].
- we just check `n` against all of these powers of two to see if it’s an anagram of any of them.
	- [[242-valid-anagram]]
