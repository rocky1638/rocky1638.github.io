# 394. Decode String

```python
class Solution:
    def decodeString(self, s: str) -> str:
        def recurse(l):
            acc = ""
            multiplier = None
            
            while l < len(s):
                c = s[l]
                if c.isnumeric():
                    multiplier = c
                    l += 1
                    while l < len(s) and s[l].isnumeric():
                        multiplier += s[l]
                        l += 1
                    multiplier = int(multiplier)
                elif c == "[":
                    next_idx, val = recurse(l+1)
                    acc += multiplier * val
                    l = next_idx
                elif c == "]":
                    return l+1, acc
                else:
                    acc += c
                    l += 1
            return len(s)-1, acc
        
        _, ans = recurse(0)
        return ans
```

- we use [[recursion]] to evaluate nested brackets.
- when we see an opening bracket, we know to go into a recursive call, and to return when we see a closing bracket.
	- each recursive call returns the next index that needs to be evaluated *(after its closing bracket)*, and the result of the [[string]] decoded within its bounds.