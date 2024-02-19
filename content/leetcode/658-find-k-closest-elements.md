# 658. Find K Closest Elements

```python
class Solution:
    def findClosestElements(self, arr: List[int], k: int, x: int) -> List[int]:
        """
        1. use binary search to find the closest element to x.
        2. do a linear scan in the window from k elements below x to k elements above x. (maybe k+1 to be safe).
        3. use a max heap to keep track of the k closest numbers we've seen.
        """

        center_idx = bisect.bisect_left(arr, x)
        lb, rb = max(0, center_idx-k-1), min(center_idx+k+1, len(arr)-1)

        heap = []
        for i in range(lb, rb+1):
            if len(heap) < k:
                heapq.heappush(heap, (-abs(x-arr[i]), arr[i]))
            else:
                diff = abs(x-arr[i])
                if (-diff > heap[0][0]) or (-diff == heap[0][0] and arr[i] < heap[0][1]):
                    heapq.heappushpop(heap, (-diff, arr[i]))
        return sorted([x[1] for x in heap])
```

- use [[binary-search]] to find the center of the window that we search linearly with our [[heap]].

[[array]]