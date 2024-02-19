---
created_at: 2022-12-06
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/palindrome-number/
---

# 9. Palindrome Number

```python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        s = str(x)

        l, r = 0, len(s)-1

        while l < r:
            if s[l] != s[r]:
                return False
            l += 1
            r -= 1

        return True
```

- convert the number to a [[string]] and use a [[two-pointers]] approach from either end to check if the string is a palindrome.

Categories:: [[string]], [[two-pointers]]
