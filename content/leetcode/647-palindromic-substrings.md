---
created_at: 2023-01-14
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/palindromic-substrings/
---

# 647. Palindromic Substrings

Given a string `s`, return _the number of **palindromic substrings** in it_.

A string is a **palindrome** when it reads the same backward as forward.

A **substring** is a contiguous sequence of characters within the string.

```python
class Solution:
    def countSubstrings(self, s: str) -> int:
        ans = 0
        
        # check for longest palindrome expanding out from l and r
        # center char is between l and r (could be one or two)
        def check(l, r):
            num_found = 0
            
            while l >= 0 and r < len(s):
                if s[l] == s[r]:
                    l -= 1
                    r += 1
                    num_found += 1
                else:
                    break
            return num_found
        
        for i in range(len(s)):
            # single char is palindrome
            ans += 1
            # expand 
            ans += check(i-1, i+1)
                
            if (i+1) < len(s) and s[i] == s[i+1]:
                ans += 1
                ans += check(i-1, i+2)
                
            i += 1
        
        return ans
```

- basically the same idea of expanding from the center as [[5-longest-palindromic-substring]] but we count number of palindromes instead of finding the longest one.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[5-longest-palindromic-substring]].

## References.

Categories:: [[dynamic-programming]], [[string]]
