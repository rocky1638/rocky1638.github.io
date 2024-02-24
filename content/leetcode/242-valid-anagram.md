---
title: 242. valid anagram
tags:
  - hashmap
---

```python
class Solution:
  def isAnagram(self, s: str, t: str) -> bool:
    return Counter(s) == Counter(t)
```

- just use a frequency map, make sure that they’re the same.
