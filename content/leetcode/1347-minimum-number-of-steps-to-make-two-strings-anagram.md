
# 1347. Minimum Number of Steps to Make Two Strings Anagram

```python
class Solution:
    def minSteps(self, s: str, t: str) -> int:
        cs = Counter(s)
        ct = Counter(t)
        
        diff_chars = set()
        num_diff = 0
        
        for key in cs:
            num_diff += abs(cs[key]-ct[key])
            diff_chars.add(key)
        for key in ct:
            if key not in diff_chars:
                num_diff += abs(cs[key]-ct[key])
                diff_chars.add(key)
        
		return num_diff // 2
```

- create a [[frequency-map]] of the two strings.
- figure out how many characters can’t directly be matched up between the two strings.
	- this number `num_diff` will always be even because the two strings are the same length, and each pair of characters are either the same or different.
- each of these pairs of different characters can be made equal in one step, so we return `num_diff // 2`.

[[string]]