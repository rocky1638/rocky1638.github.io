# 287. Find the Duplicate Number

## Marking numbers negative.

```python
class Solution:
    def findDuplicate(self, nums: List[int]) -> int:
        for i, num in enumerate(nums):
            if nums[abs(num)] < 0:
                return abs(num)
            nums[abs(num)] *= -1
```

- if we see a number, we mark that index in the array as negative.
- if we see that number again, we’ll know we’ve seen it before if it has already been marked negative.
- this approach is linear time and constant space, but modifies the original array.

## Binary search.

```python
class Solution:
    def findDuplicate(self, nums: List[int]) -> int:
        # 'low' and 'high' represent the range of values of the target
        low = 1
        high = len(nums) - 1
        
        while low <= high:
            cur = (low + high) // 2
            count = 0

            # Count how many numbers are less than or equal to 'cur'
            count = sum(num <= cur for num in nums)
            if count > cur:
                duplicate = cur
                high = cur - 1
            else:
                low = cur + 1
                
        return duplicate
```

- the key insight here is that in a sorted array without duplicates that contains all the positive numbers up to $n$, any given number $x$ has $x$ numbers that are less than or equal to it to the left of it.
	- if this array has duplicates added, then any number $x$ that has duplicates *(and any number larger than it)* will have more than $x$ other numbers that are less than or equal to it.
	- thus, the smallest number that has more numbers less than or equal to it will be the duplicated number.
- we can implement this approach using [[binary-search]], counting the count of numbers less than or equal at each step of the way.

[[array]]