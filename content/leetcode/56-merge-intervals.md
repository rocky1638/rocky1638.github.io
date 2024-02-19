---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/merge-intervals/
---

# 56. Merge Intervals

```python
class Solution:
    def merge(self, intervals: List[List[int]]) -> List[List[int]]:
        # sort by starting time
        intervals.sort(key=lambda x: x[0])
        
        merged = [intervals[0]]
        
        for interval in intervals[1:]:
            # if interval overlaps with most recent in merged
            if merged[-1][1] >= interval[0]:
                merged[-1][1] = max(merged[-1][1], interval[1])
            else:
                merged.append(interval)
        return merged
```

- classic [[interval]] problem.
- sort the intervals by starting time.
- push new intervals into `merged` array.
- if the next interval overlaps, update the top element of `merged`.

Categories:: [[sorting]], [[array]], [[interval]]
