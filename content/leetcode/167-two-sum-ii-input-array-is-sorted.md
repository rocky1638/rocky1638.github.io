---
created_at: 2023-01-03
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/
---

# 167. Two Sum II – Input Array Is Sorted

```python
class Solution:
    def twoSum(self, numbers: List[int], target: int) -> List[int]:
        l, r = 0, len(numbers)-1

        while l < r:
            val = numbers[l] + numbers[r]
            if val == target:
                return [l + 1, r + 1]
            elif val < target:
                l += 1
            else:
                r -= 1
```

- use [[two-pointers]] method to move inwards.
	- move left pointer up if the value is too small, right pointer down if value is too big.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[1-two-sum]].
- [[15-3sum]].

## References.

Categories:: [[two-pointers]], [[array]]
