# 438. Find All Anagrams in a String

```python
class Solution:
    def findAnagrams(self, s: str, p: str) -> List[int]:
        freq = Counter(s[:len(p)])
        pfreq = Counter(p)
        
        ans = []
        
        if freq == pfreq:
            ans.append(0)
        
        for i in range(1, len(s)-len(p)+1):
            freq[s[i-1]] -= 1
            freq[s[i+len(p)-1]] += 1
            
            if freq == pfreq:
                ans.append(i)
        return ans
```

- classic [[sliding-window]] problem using a [[frequency-map]].
- when the [[frequency-map]] of the string `p` matches with the frequency of the window we’re looking at in `s`, we add the index to the `ans` array.

[[string]]