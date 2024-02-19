# 844. Backspace String Compare

```python
class Solution:
    def backspaceCompare(self, s: str, t: str) -> bool:
        ss = []
        tt = []
        
        for c in s:
            if c == "#":
                if ss:
                    ss.pop()
            else:
                ss.append(c)
        
        for c in t:
            if c == "#":
                if tt:
                    tt.pop()
            else:
                tt.append(c)

        return ss == tt
```

- we use [[stack]] to figure out what the final string is with all the backspaces.
- just compare the two [[array]] at the end.

[[string]]