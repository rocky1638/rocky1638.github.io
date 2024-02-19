# 611. Valid Triangle Number

## Binary search for hypotenuse.

```python
class Solution:
    def triangleNumber(self, nums: List[int]) -> int:
        nums.sort()
        ans = 0
        
        for i in range(len(nums)-2):
            for j in range(i+1, len(nums)-1):
                a = nums[i]
                b = nums[j]
                c = a + b
                
                # binary search for first number thats too big
                l, r = j + 1, len(nums)-1
                
                while l <= r:
                    m = (l+r)//2
                    
                    if (m == len(nums)-1 and nums[m] < c) or (nums[m] < c and nums[m+1] >= c):
                        ans += m - j
                        break
                    elif nums[m] >= c:
                        r = m - 1
                    else:
                        l = m + 1
            
        return ans
```

- the idea here is to sort the [[array]] first, and then to check each pair of shorter sides, and to find all the third sides that can be smaller than the sum of the two shorter sides.
- we use [[binary-search]] to find the cutoff and add all the valid values.
- this has runtime $O(n^2\log(n))$, and times out.

## Two pointers.
 
```python
class Solution:
    def triangleNumber(self, nums: List[int]) -> int:
        nums.sort()
        n = len(nums)
        ans = 0
        
        for k in range(2, n):
            i = 0
            j = k - 1
            while i < j:
                if nums[i] + nums[j] > nums[k]:
                    ans += j - i
                    j -= 1
                else:
                    i += 1
        return ans
```

- we still use [[sorting]], but we instead fix the longest face, and move inwards with [[two-pointers]] to find all the possible pairs of shorter sides that can satisfy the longer side.
- because the array is sorted, if $a+b > c$, then we move our right pointer inwards until it isn’t, and then move our left pointer to the right until the condition is satisfied again.
	- reminiscent of [[sliding-window]] logic.
- runtime is $O(n^2)$.