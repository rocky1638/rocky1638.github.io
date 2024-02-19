# 242. Valid Anagram

```python
from collections import Counter

class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        return Counter(s) == Counter(t)
```

- just use a [[frequency-map]], make sure that they’re the same.

[[hashmap]]