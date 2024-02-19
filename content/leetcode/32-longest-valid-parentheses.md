---
created_at: 2023-01-03
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/longest-valid-parentheses/
---

# 32 Longest Valid Parentheses

```python
class Solution:
    def longestValidParentheses(self, s: str) -> int:
        """
        note that every index in stack is offset to the left by one,
        to make finding the length between two indices easier.
        (normally you'd have to do r - l + 1, but in our case, l is already l-1).
        """
        # we initialize with -1 for the case where the
        # valid substring starts at the beginning of s
        stack = [-1]
        ans = 0

        # stack stores the index BEFORE where
        # a valid substring could start

        for i in range(len(s)):
            if s[i] == "(":
                stack.append(i)
            else:
                stack.pop()
                if not stack:
                    stack.append(i)
                else:
                    ans = max(ans, i - stack[-1])
        return ans
```

## Video walkthrough.

- [01:15](https://www.youtube.com/watch?v=q56S5NIqjdE#t=75.41176298092651) intuition of using a stack for these [[20-valid-parentheses]] type problems.
- [02:14](https://www.youtube.com/watch?v=q56S5NIqjdE#t=134.05763413160705) intuition of storing the index numbers of the open parentheses in the string.
- [05:50](https://www.youtube.com/watch?v=q56S5NIqjdE#t=350.85294) second solution.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

 - [[20-valid-parentheses]].

## References.

Categories:: [[stack]], [[string]]
