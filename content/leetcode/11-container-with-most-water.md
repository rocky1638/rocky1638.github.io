---
created_at: 2022-11-22
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/container-with-most-water/
---

# 11. Container with Most Water

```python
class Solution:
    def maxArea(self, height: List[int]) -> int:
        ans = 0
        
        l, r = 0, len(height)-1
        
        while l < r:
            minheight = min(height[l], height[r])
            ans = max(ans, minheight * (r-l))
            
            # how do we move in? greedily keep the larger one
            if height[l] < height[r]:
                l += 1
            else:
                r -= 1
        return ans
```

- we use [[two-pointers]] to move gradually inward from the outside, keeping track of most water stored in `ans`.
- we always move inward with the shorter of the two walls!
	- we can prove this [[greedy]] approach by thinking about the contrary.
	- if we moved in with the taller wall, we would always guarantee that our stored water would be less, because the horizontal distance is decreasing, and even if we found a taller wall, we would still be equally limited by the shorter wall *(that we did not move inwards from).*
	- therefore, we must always move the shorter wall to have a chance at increasing `ans`.

Categories:: [[array]], [[two-pointers]], [[greedy]]
