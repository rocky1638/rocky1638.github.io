---
created_at: 2022-11-15
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/add-binary/
---

# 67. Add Binary

```python
class Solution:
    def addBinary(self, a: str, b: str) -> str:
        i, j = len(a)-1, len(b)-1
        ans = ""
        carrying = False
        
        while i>=0 or j>=0:
            val = 0
            if i >= 0:
                if a[i] == "1":
                    val += 1
                i -= 1
                    
            if j >= 0:
                if b[j] == "1":
                    val += 1
                j -= 1
                    
            if val == 2 and carrying:
                ans += "1"
            else:
                if carrying:
                    val += 1
                    carrying = False
                    
                if val == 2:
                    carrying = True
                    ans += "0"
                elif val == 1:
                    ans += "1"
                else: # val == 0
                    ans += "0"
        
        if carrying:
            ans += "1"
        
        return ans[::-1]
```

- just a bunch of annoying logic for doing addition by hand.

Categories:: [[string]], [[math]]
