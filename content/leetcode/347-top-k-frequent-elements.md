---
created_at: 2023-01-03
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/top-k-frequent-elements/
---

# 347. Top K Frequent Elements

```python
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]:
        cnt = collections.Counter(nums)
        heap = []

        for val, count in cnt.items():
            if len(heap) < k:
                heapq.heappush(heap, (count, val)) 
            else:
                if count > heap[0][0]:
                    heapq.heappushpop(heap, (count, val))

        return [x[1] for x in heap]
```

- we use a min-heap of length $k$ to store the best most frequent elements that we get from a `Counter` or frequency map.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[heap]], [[frequency-map]], [[array]]
