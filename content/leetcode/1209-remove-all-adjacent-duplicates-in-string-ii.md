# 1209. Remove All Adjacent Duplicates in String II

```python
class Solution:
    def removeDuplicates(self, s: str, k: int) -> str:
        # [char, count]
        stack = []
        
        for c in s:
            if not stack or stack[-1][0] != c:
                stack.append([c, 1])
            else:
                stack[-1][1] += 1
            
            while stack and stack[-1][1] >= k:
                stack[-1][1] -= k
                if stack[-1][1] == 0:
                    stack.pop()
        
        ans = ""
        for char, count in stack:
            for c in range(count):
                ans += char
                
        return ans
```

- we keep pushing each new character into a [[stack]], and delete all blocks of `k` characters as they come up.
- we store tuples of `[char, count]` instead of just characters in order to improve the speed of checking for blocks from $O(n)$ to $O(1)$.

[[string]]