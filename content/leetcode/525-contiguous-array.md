# 525. Contiguous Array

```python
class Solution:
    def findMaxLength(self, nums: List[int]) -> int:
        """
        - Iterate through the array, and keep an up-and-down tally that goes up by 1
          when the value is 1 and down by 1 when the value is 0
        - If at any point this tally is 0, then the array from the start up to this point is
          balanced.
        - The first time we see a non-zero count, store it in map.
        - The next time we see the same count, we know that the subarray from that previous count
          to now must have been balanced (think hills and valleys)
        """

        ans = 0
        d = {}
        count = 0

        for i, num in enumerate(nums):
            if num == 0: count -= 1
            if num == 1: count += 1

            if count == 0:
                ans = i+1

            else:
                if count in d:
                    ans = max(ans, i-d[count])
                else:
                    d[count] = i
        return ans
```

- i originally thought to use [[prefix-sum]] pattern, but it timed out likely due to the $O(n)$ iteration through the prefix array for each value in the array.
- it is best to think about this problem like a path where each 1 makes you go uphill, and each 0 makes you go downhill.
	- we start at elevation of 0, and if we ever reach elevation 0 again, we know that we’ve traversed a balanced section.
	- also, the first time we reach a new elevation, we should store where it is.
		- the next time we reach this **same** elevation, we know that portion we’ve walked is balanced!

[[hashmap]], [[array]]