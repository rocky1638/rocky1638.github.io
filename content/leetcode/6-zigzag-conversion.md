---
created_at: 2022-12-06
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/zigzag-conversion/
---

# 6. Zigzag Conversion

```python
class Solution:
    def convert(self, s: str, numRows: int) -> str:
        if numRows == 1:
            return s

        rows = collections.OrderedDict()
        for i in range(numRows):
            rows[i] = []
        ci = 0
        curcol = 0
        
        while ci < len(s):
            # full column
            if curcol % (numRows-1) == 0:
                for j in range(numRows):
                    if ci < len(s):
                        rows[j].append(s[ci])
                        ci += 1
            else:
                row = (numRows-1) - (curcol % (numRows-1))
                rows[row].append(s[ci])
                ci += 1
            curcol += 1
        
        ans = ""
        for key in rows:
            ans += "".join(rows[key])
        return ans
```

- just a lot of funky [[string]] manipulation.
- i use a [[hashmap]] to store a list of the values of each row.

Categories:: [[string]], [[hashmap]]
