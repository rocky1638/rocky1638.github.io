---
created_at: 2022-11-25
type: leetcode
aliases: []
difficulty: 🔴
needs_review: true
link: https://leetcode.com/problems/largest-rectangle-in-histogram/
---

# 84. Largest Rectangle in Histogram

Given an array of integers `heights` representing the histogram's bar height where the width of each bar is `1`, return _the area of the largest rectangle in the histogram_.

```python
class Solution:
    def largestRectangleArea(self, heights: List[int]) -> int:
        ans = 0
        stack = [] # (index, height)

        for i, h in enumerate(heights):
            # if previous height on stack is bigger
            # it can't be extended anymore
            prev_i = None
            while len(stack) and stack[-1][1] > h:
                prev_i, prev_height = stack.pop()
                ans = max(ans, (i-prev_i) * prev_height)

            # if we popped some elements off, this new
            # bar can essentially be extended "back" through
            # all the bars that we popped off
            if prev_i is not None:
                stack.append((prev_i, h))
            else:
                stack.append((i, h))
        
        # deal with bars that managed to extend
        # to the end of the histogram
        n = len(heights)
        for i, h in stack:
            ans = max(ans, (n-i)*h)

        return ans
```

- we use a stack, and while iterating through the bars, consider how far we can extend the current bar to make a square _(where the square’s left edge is the current bar)_.
- we know we can extend a bar to the right as long as the bars to the right are equal or greater height.
- maintain a monotonic stack.
	- everytime we see a bar that is shorter than the previous bar, we pop the previous bars and calculate the biggest squares they produced, because they can longer be extended to the right as per the logic above.
		- see the video notes for more detailed indexing notes.
	- at the end, any bars that are still on the stack were able to be extended to the end of the histogram, calculate areas accordingly.

## Neetcode video walkthrough.

- [00:20](https://www.youtube.com/watch?v=zx5Sw9130L0#t=20) problem explanation.
- [01:01](https://www.youtube.com/watch?v=zx5Sw9130L0#t=61) optimization intuition, we can’t extend a square to the right if the next bar is shorter.
- [01:42](https://www.youtube.com/watch?v=zx5Sw9130L0#t=102.43211599427795) we have to take the shortest bar for our rectangle height.
- [02:44](https://www.youtube.com/watch?v=zx5Sw9130L0#t=164.0992448073578) **if the heights are in increasing order, we can always extend a square to the right!**
- [02:55](https://www.youtube.com/watch?v=zx5Sw9130L0#t=175.94014520027162) monotonic stack intuition and walkthrough.
- [04:35](https://www.youtube.com/watch?v=zx5Sw9130L0#t=275.1020369294281) one more example.
- [05:50](https://www.youtube.com/watch?v=zx5Sw9130L0#t=350.0562180705719) algorithm explanation and walkthrough.
- [07:39](https://www.youtube.com/watch?v=zx5Sw9130L0#t=450) tricky indexing.
	- when we pop off bars, we have to consider that this shorter bar could’ve also been extended _left_ through the popped bars.
- [08:49](https://www.youtube.com/watch?v=zx5Sw9130L0#t=529.1710090724793) we’re always considering the square that **starts** from the index we’re popping.
- [11:05](https://www.youtube.com/watch?v=zx5Sw9130L0#t=665.2252799160767) elements that are left in the stack were able to be extended to the end of the histogram, compute the area accordingly.
- [14:03](https://www.youtube.com/watch?v=zx5Sw9130L0#t=843.5523589465943) writing the code.

Categories:: [[array]], [[stack]], [[monotonic-stack]]
