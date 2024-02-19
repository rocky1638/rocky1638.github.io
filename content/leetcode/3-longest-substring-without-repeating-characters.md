---
created: 2022-11-16
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/longest-substring-without-repeating-characters/
---

# 3. Longest Substring Without Repeating Characters

```python
from collections import defaultdict

class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        l = 0
        count = 0
        ans = 0
        d = defaultdict(int)
        
        for r in range(len(s)):
            d[s[r]] += 1
            count += 1
            
            while d[s[r]] > 1:
                d[s[l]] -= 1
                l += 1
                count -= 1
               
            ans = max(ans, count)
        
        return ans
```

- classic [[sliding-window]] approach.
- we slide the right pointer forward until we see a duplicate character.
- then, we slide the left pointer forward until that character is no longer duplicated.
- keep a running max tally to return.

Categories:: [[string]], [[hashmap]], [[sliding-window]]
