# 191. Number of One Bits

```python
class Solution:
    def hammingWeight(self, n: int) -> int:
        ans = 0
        mask = 1

        for _ in range(32):
            if mask & n > 0:
                ans += 1
            mask <<= 1
            
        return ans
```

- a lot of using bitwise operators, including bitshift left and bitwise and.
- we use a mask that always has a one in each position of the 32 bits.
	- for each mask, if our number is above zero when we bitwise and with the mask, we can increment our answer.

[[math]], [[bit-manipulation]]