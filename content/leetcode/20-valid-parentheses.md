---
created_at: 2022-11-11
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/valid-parentheses/
---

# 20. Valid Parentheses

```python
class Solution:
    def isValid(self, s: str) -> bool:
        stack = []
        m = {
            ')': '(',
            '}': '{',
            ']': '['
        }
        
        for c in s:
            if c in ['(', '{', '[']:
                stack.append(c)
            elif len(stack) == 0 or c in [')', '}', ']'] and stack[-1] != m[c]:
                return False
            else:
                stack.pop()
        
        return len(stack) == 0
```

- [[stack]] to store the brackets.
- [[hashmap]] for ease of coding.
- just loop through the string.
- edge cases for ill-formed strings *(start with closing bracket, not enough closing brackets)*.

Categories:: [[stack]], [[hashmap]], [[string]]
