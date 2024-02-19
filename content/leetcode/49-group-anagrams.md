---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/group-anagrams/
---

# 49. Group Anagrams

```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        d = collections.defaultdict(list) 
        for s in strs:
            key = str(sorted(s))
            d[key].append(s) 
        return d.values()
```

- use a [[hashmap]] and group the strings by sorted values.
- just return the groupings at the end.

Categories:: [[hashmap]], [[string]], [[sorting]]
