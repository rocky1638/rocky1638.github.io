# 238. Product of Array Except Self

```python
class Solution:
    def productExceptSelf(self, nums: List[int]) -> List[int]:
        pre = [0]*len(nums)
        post = [0]*len(nums)
        pre[0] = nums[0]
        post[-1] = nums[-1]
        
        for i in range(1, len(nums)):
            pre[i] = nums[i] * pre[i-1]
        
        for i in reversed(range(len(nums)-1)):
            post[i] = nums[i] * post[i+1]
        
        ans = []
        for i in range(len(nums)):
            pre_prod = pre[i-1] if i-1 >= 0 else 1
            post_prod = post[i+1] if i+1 < len(nums) else 1
            
            ans.append(pre_prod * post_prod)
        
        return ans
```

- we keep a prefix and postfix array of products of the array, so that we can just multiple specific prefix products and postfix products at each index to find the product of the total array *(excluding one value each time)*.
- classic example of using extra space to save on time.

[[prefix-sum]], [[array]]