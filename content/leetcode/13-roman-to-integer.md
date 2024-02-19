---
created_at: 2022-12-08
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/roman-to-integer/
---

# 13. Roman to Integer

```python
class Solution:
    def romanToInt(self, s: str) -> int:
        d = {
            "I": 1,
            "V": 5,
            "X": 10,
            "L": 50,
            "C": 100,
            "D": 500,
            "M": 1000,
        }

        ans = 0
        prev = None
        for c in s:
            ans += d[c]
            if prev and d[c] > d[prev]:
                ans -= 2 * d[prev]
            prev = c

        return ans
        
```

- make a [[hashmap]] to map the characters to their numerical values.
- just keep adding the values in the [[string]], unless it’s in reverse order in which case we subtract.

Categories:: [[hashmap]], [[string]]
