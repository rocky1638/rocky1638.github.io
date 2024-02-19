---
created_at: 2022-11-24
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/minimum-window-substring/
---

# 76. Minimum Window Substring

```python
class Solution:
    def minWindow(self, s: str, t: str) -> str:
        tcount = Counter(t)
        wincount = Counter()
        l = 0
        ans = ""
        best = float("inf")
        
        # expand r forward until window is valid
        # then move l forward until invalid
        for r in range(len(s)):
            wincount[s[r]] += 1
            while all(wincount[x] >= tcount[x] for x in tcount):
                winlength = r-l+1
                if winlength < best:
                    ans = s[l:r+1]
                    best = len(ans)
                wincount[s[l]] -= 1
                l += 1
        return ans
```

- classic [[sliding-window]] approach using [[frequency-map]].
- we slide our right pointer over until we have a valid string, then try to shrink our window until it is invalid again.

Categories:: [[sliding-window]], [[frequency-map]], [[hashmap]], [[string]]
