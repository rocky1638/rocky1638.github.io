---
created_at: 2023-01-01
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/longest-common-prefix/
---

# 14. Longest Common Prefix

```python
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        ans = 0
        
        for i, c in enumerate(strs[0]):
            for s in strs[1:]:
                if i >= len(s) or s[i] != c:
                    return strs[0][:i]
            ans += 1
        return strs[0][:ans]
```

- we choose a random [[string]] in the list, and go through its characters.
	- check if the same letter in the prefix exists in every other string.
	- whenever one check fails, we return the prefix we’ve built up.
- it’s also possible to solve this with a [[divide-and-conquer]] approach.

Categories:: [[string]], [[divide-and-conquer]]
