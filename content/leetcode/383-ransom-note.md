# 383. Ransom Note

```python
class Solution:
    def canConstruct(self, ransomNote: str, magazine: str) -> bool:
        cr, cm = Counter(ransomNote), Counter(magazine)
        
        for key in cr:
            if key in cm and cm[key] >= cr[key]:
                continue
            else:
                return False
        
        return True
```

- create a [[frequency-map]] for both of the [[string|strings]].
- make sure that every character in ransom note appears at least that many time in the magazine.