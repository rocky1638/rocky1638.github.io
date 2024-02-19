---
created_at: 2022-11-15
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/insert-interval/
---

# 57. Insert Interval

```python
class Solution:
    ans = []
    
    def appendAndMergeIfNecessary(self, x1, x2):
        if len(self.ans) == 0 or x1 > self.ans[-1][1]: # no overlap
            self.ans.append([x1, x2])
        else:
            self.ans[-1] = [min(x1, self.ans[-1][0]), max(x2, self.ans[-1][1])]
        
    def insert(self, intervals: List[List[int]], newInterval: List[int]) -> List[List[int]]:  
        self.ans = []
        i = 0
        while i < len(intervals):
            # before newInterval
            if intervals[i][0] < newInterval[0]:
                self.ans.append(intervals[i])
                i += 1
            else:
                break
        
        self.appendAndMergeIfNecessary(newInterval[0], newInterval[1])
        
        while i < len(intervals):
            self.appendAndMergeIfNecessary(intervals[i][0], intervals[i][1])
            i += 1
        
        return self.ans
```

- make another array `ans`, and first append all the intervals that come strictly before the `newInterval`.
- then for the rest of the intervals including `newInterval`, we will merge with the interval at the end of the array `ans` if they overlap.

Categories:: [[interval]], [[array]]
