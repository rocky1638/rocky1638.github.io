---
created_at: 2022-11-11
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/valid-palindrome/
---

# 125. Valid Palindrome

```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        filtered = ''.join(list(filter(lambda c: c.isalnum(), list(s)))).lower()
        return filtered == filtered[::-1]
```

- just filter the [[string]] the correct way and check if the reverse is read the same way.

Categories:: [[string]]
