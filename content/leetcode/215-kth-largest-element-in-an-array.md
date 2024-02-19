---
created_at: 2022-12-25
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/kth-largest-element-in-an-array/
---

# 215. Kth Largest Element in an Array

Given an integer array `nums` and an integer `k`, return _the_ `kth` _largest element in the array_.

Note that it is the `kth` largest element in the sorted order, not the `kth` distinct element.

You must solve it in `O(n)` time complexity.

```python
class Solution:
    def findKthLargest(self, nums: List[int], k: int) -> int:
        heap = []
        for num in nums:
            if len(heap) < k:
                heapq.heappush(heap, num)
            elif num > heap[0]:
                heapq.heappushpop(heap, num)
        return heap[0]
```

- simple [[heap]] problem.
- keep a min-heap of the `k` largest elements of the [[array]].
- at the end, the kth largest element will be at the top of the heap.

Categories:: [[heap]], [[array]]
