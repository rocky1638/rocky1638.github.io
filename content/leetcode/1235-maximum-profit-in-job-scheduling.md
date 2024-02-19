# 1235. Maximum Profit in Job Scheduling

## Dynamic programming with `OrderedDict` & binary search.

```python
class Solution:
    def jobScheduling(self, startTime: List[int], endTime: List[int], profit: List[int]) -> int:
        max_ending_at_time = collections.OrderedDict()
        max_ending_at_time[1] = 0
        
        def findNearestKey(time):
            keys = list(max_ending_at_time.keys())
            key_idx = bisect.bisect_left(keys, time)
            if key_idx < len(keys) and keys[key_idx] == time:
                return keys[key_idx]
            else:
                return keys[key_idx-1]
        
        # sort by ending time, tiebreak on profit (descending)
        intervals = sorted([[s, e, pr] for s, e, pr in zip(startTime, endTime, profit)], key=lambda x: (x[1], -x[2]))
        
        # dp[i] = max profit using the first i jobs (sorted by end time)
        dp = []
        
        for s, e, p in intervals:
            # max_ending_at_time(findNearestKey(s)) returns the max profit ending at start time (or before)
            val = p + max_ending_at_time[findNearestKey(s)]
            dp.append(max(val, dp[-1] if dp else 0))
            max_ending_at_time[e] = dp[-1]
        return dp[-1]
```

- my idea here was to store the maximum profit ending at time `i` in `dp[i]`.
- sort the intervals by `endTime`, and then iterate through, taking the maximum of not using the current job, or using the current job and the best profit ending at or before the start time of the current job.

![[1235-e1.excalidraw]]
- consider `t=4` when we are looking at the red block.
	- we can choose to take it, in which case our profit is 6 plus the max profit ending at 2, which is 0.
	- we can not take it, in which case we just use the max profit at `t=3`, which is 8.
		- i kept track of these profits by time in an `OrderedDict` so i could binary search on its keys to find the nearest time that was equal or less than the starting time.

## Recursion with memoization

```python
class Solution:
    def jobScheduling(self, starts, ends, profits):
        start, end, profit = 0, 1, 2
        jobs = list(zip(starts, ends, profits))
        jobs.sort(key=lambda x: x[start])
        
        memo = {}
        
        def dp(i):
            if i not in memo:
                if i >= len(jobs):
                    ans = 0
                else:
                    nxt = bisect.bisect_left(jobs, jobs[i][end], key=lambda x: x[start])
                    # (use current job, or skip it)
                    ans = max(jobs[i][profit] + dp(nxt), dp(i + 1))
                memo[i] = ans
            return memo[i]
        
        return dp(i=0)
```

- at each step in our [[recursion]] top-down, we decide to either use the current job or not.
	- if we decide to use the current job, we [[binary-search]] for the next available job index because our job [[array]] is sorted by `startTime`.

[[sorting]], [[dynamic-programming]]