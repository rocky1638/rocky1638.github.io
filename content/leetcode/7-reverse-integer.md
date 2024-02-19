---
created_at: 2023-01-01
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/reverse-integer/
---

# 7 Reverse Integer

```python
class Solution:
    def reverse(self, x: int) -> int:
        isNegative = False
        if x < 0:
            isNegative = True
            x = abs(x)

        ans = 0
        while x > 0:
            last_digit = x % 10
            ans *= 10
            ans += last_digit

            if ans > 2 ** 31: return 0

            x = x // 10
        return -ans if isNegative else ans
```

- use some [[math]] including modulus and integer division to build up the answer in reverse.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[math]]
