---
created: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/longest-palindromic-substring/
---

# 5. Longest Palindromic Substring

```python
class Solution:
    def longestPalindrome(self, s: str) -> str:
        ans = ""
        
        # check for longest palindrome expanding out from l and r
        # center char is between l and r (could be one or two)
        def check(l, r, center_length):
            tally = center_length
            
            while l >= 0 and r < len(s):
                if s[l] == s[r]:
                    l -= 1
                    r += 1
                    tally += 2
                else:
                    break
            return l+1, r-1
        
        for i in range(len(s)):
            lb, rb = check(i-1, i+1, 1)
            if (rb-lb+1) > len(ans):
                ans = s[lb:rb+1]
                
            if (i+1) < len(s) and s[i] == s[i+1]:
                lb, rb = check(i-1, i+2, 2)
                if (rb-lb+1) > len(ans):
                    ans = s[lb:rb+1]
                
            i += 1
        
        return ans
```

- we iterate through the [[string]], and for each character, we check for the longest possible substring that centers at that character.
	- also make sure to check for palindromes that have a pair of the same character at the center.

Categories:: [[dynamic-programming]], [[string]]
