---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/daily-temperatures/
---

# 739. Daily Temperatures

Given an array of integers `temperatures` represents the daily temperatures, return _an array_ `answer` _such that_ `answer[i]` _is the number of days you have to wait after the_ `ith` _day to get a warmer temperature_. If there is no future day for which this is possible, keep `answer[i] == 0` instead.

```python
class Solution:
    def dailyTemperatures(self, temperatures: List[int]) -> List[int]:
        """
        use a stack iterating forwards?

        we go forwards in the array
        as we go forwards, if the current temperature is greater
        than what is already on the stack, pop off stack and add to array
        """
        n = len(temperatures)
        ans = [0] * n

        stack = []

        for i, temp in enumerate(temperatures):
            while len(stack) and temp > temperatures[stack[-1]]:
                idx = stack.pop()
                ans[idx] = i-idx
            stack.append(i)
        return ans
```

- my least favorite concept, the [[monotonic-stack]].
- we iterate through the [[array]], and append the temperatures to our stack.
	- for each value in the [[stack]], we see if the current value is larger.
	- if the current value is larger, that means that the current value is the first value after that stack value that is larger than it.
		- we record the index difference, and pop this stack value off of the stack because it’s now been accounted for.

Categories:: [[stack]], [[monotonic-stack]], [[array]]
