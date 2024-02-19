---
created_at: 2022-11-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/word-break/
---

# 139. Word Break

```python
class Solution:
    def wordBreak(self, s: str, wordDict: List[str]) -> bool:
        wordSet = set(wordDict) # for faster lookup
        
        # dp[i] represents if prefix string with length i satisfies the condition
        # base case empty string satisfies
        dp = [True]
        
        for i in range(len(s)):
            j = i
            valid = False
            while j >= 0:
                if dp[j]:
                    valid = s[j:i+1] in wordSet
                    if valid:
                        dp.append(True)
                        break
                j -= 1
            if not valid:
                dp.append(False)
            i += 1
        
        return dp[-1]
```

- we use [[dynamic-programming]].
- `dp[i]` represents whether the substring with length `i` can be broken up into valid words.
	- at each iteration, we can look back in our `dp` array and if we see a `True` value, we just have to check the additional substring to see if it is valid.
	- note that we need to check all the previous `True` entries in `dp`.

Categories:: [[dynamic-programming]], [[string]]
