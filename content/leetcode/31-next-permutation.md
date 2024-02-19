---
created_at: 2022-12-09
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/next-permutation/
---

# 31. Next Permutation

```python
class Solution:
    def nextPermutation(self, nums: List[int]) -> None:
        """
        - we know the suffix section that is all descending is maximized already.
        - the number right before the start of the descending sequence is the one that is going to be swapped.
        - it will be swapped with the smallest number in the descending sequence that is larger than it.
        - the descending sequence will then be flipped to be ascending.
        """ 
        if len(nums) == 1:
            return

        before_desc = None

        # from the right, find the end of the descending sequence.
        r = len(nums) - 1
        while r > 0:
            # r-1 is the number before the descending sequence. 
            if nums[r] > nums[r-1]:
                before_desc = r-1 
                break
            r -= 1
        # this means everything is descending, largest possible, return smallest
        if before_desc is None:
            nums.reverse()
            return
            
        to_swap = None
        r = len(nums) - 1
        while r >= 0:
            # this is guaranteed to hit because otherwise entire number
            # would be descending
            if nums[r] > nums[before_desc]:
                to_swap = r
                break
            r -= 1

        # swap before_desc and to_swap
        nums[to_swap], nums[before_desc] = nums[before_desc], nums[to_swap]

        # flip the descending section
        l, r = before_desc + 1, len(nums) - 1
        while l < r:
            nums[l], nums[r] = nums[r], nums[l]
            l += 1
            r -= 1
```

- this is in the same vertical as [[46-permutations]], but the solution really isn’t related to it.
- you just have to figure out the pattern of how to find the next largest permutation number.
- the logic is explained in the comments at the top of the code.

## Related.

- [[46-permutations]].

Categories:: [[two-pointers]], [[array]]
