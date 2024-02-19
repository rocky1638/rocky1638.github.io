# 217. Contains Duplicate

```python
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        seen = set()
        
        for n in nums:
            if n in seen:
                return True
            seen.add(n)
        
        return False
```

- iterate through the [[array]] and keep track of values that we’ve seen.