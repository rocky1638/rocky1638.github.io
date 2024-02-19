# 1614. Maximum Nesting Depth of the Parentheses

```python
class Solution:
    def maxDepth(self, s: str) -> int:
        ans = 0
        count = 0
        for c in s:
            if c == "(":
                count += 1
                ans = max(ans, count)
            elif c == ")":
                count -= 1
        return ans
```

- just increment the depth when we see an opening bracket, and decrement when we see a closing bracket.

[[string]]