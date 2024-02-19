---
created_at: 2022-12-31
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/decode-ways/
---

# 91. Decode Ways

```python
class Solution:
    def numDecodings(self, s: str) -> int:
        m = {
            "1": "A",
            "2": "B",
            "3": "C",
            "4": "D",
            "5": "E",
            "6": "F",
            "7": "G",
            "8": "H",
            "9": "I",
            "10": "J",
            "11": "K",
            "12": "L",
            "13": "M",
            "14": "N",
            "15": "O",
            "16": "P",
            "17": "Q",
            "18": "R",
            "19": "S",
            "20": "T",
            "21": "U",
            "22": "V",
            "23": "W",
            "24": "X",
            "25": "Y",
            "26": "Z",
        }

        if len(s) == 0 or s[0] == "0":
            return 0

        # dp[i] = number of ways for string ending at i
        dp = [1]
        for i in range(1, len(s)):
            temp = 0
            if s[i] in m:
                temp += dp[i-1]
            if s[i-1]+s[i] in m:
                temp += dp[i-2]
            dp.append(temp)
        return dp[-1]
```

- we use standard [[dynamic-programming]], where $dp[i]$ is equal to the number of possible decoding ways with the string ending at $i$.
- just build up the $dp$, either using a single-digit number or a two-digit number.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[array]], [[dynamic-programming]]
