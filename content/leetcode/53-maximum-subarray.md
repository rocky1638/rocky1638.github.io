---
created_at: 2022-11-15
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/maximum-subarray/
---

# 53. Maximum Subarray

```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        ans = float("-inf")
        maxendinghere = 0
        
        for n in nums:
            maxendinghere = max(n, maxendinghere + n)
            ans = max(ans, maxendinghere)
        
        return ans
```

- this question is essentially [[dynamic-programming]].
- at each index of the array, we ask ourselves what the maximum subarray is that has its right bound at the current index.
	- we can either add on to the maximum subarray that ended at the previous index, or start a new subarray.
	- `maxendinghere = max(n, maxendinghere+n)`

essentially, if $A_i$ is equal to the value of the array at index $i$ and $M_i$ is equal to the maximum subarray ending at index $i$, then our optimization function is

$$
M_i=
\begin{cases}
A_i \text{ if } i=0 \\
\max(A_i, M_{i-1}+A_i) \text{ otherwise}
\end{cases}
$$

Categories:: [[array]], [[dynamic-programming]]
