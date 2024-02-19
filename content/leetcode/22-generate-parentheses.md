---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/generate-parentheses/
---

# 22. Generate Parentheses

```python
class Solution:
    def generateParenthesis(self, n: int) -> List[str]:
        o = 0
        c = 0
        acc = []
        ans = []

        def recurse():
            nonlocal c
            nonlocal o
            if c == n:
                ans.append("".join(acc))
            else:
                if o < n:
                    acc.append("(")
                    o += 1
                    recurse()
                    o -= 1
                    acc.pop()
                if c < o:
                    acc.append(")")
                    c += 1
                    recurse()
                    c -= 1
                    acc.pop()


        recurse()
        return ans
```

- classic [[backtracking]] problem, very similar to [[46-permutations]].

## Related.

- [[46-permutations]].

Categories:: [[backtracking]], [[string]]
