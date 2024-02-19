# 973. K Closest Points to Origin

```python
import heapq

class Solution:
    def calculateDistance(self, x, y):
        return sqrt(x**2 + y**2)
    
    def kClosest(self, points: List[List[int]], k: int) -> List[List[int]]:
        heap = []
        heapq.heapify(heap)
        
        for point in points:
            distance = self.calculateDistance(point[0], point[1])

            if len(heap) < k:
                heapq.heappush(heap, (-distance, point))
            elif distance < -heap[0][0]:
                heapq.heappop(heap)
                heapq.heappush(heap, (-distance, point))
        
        return [val[1] for val in heap]
```

- we keep a max-heap of length `k`, and iterate through the points.
- if the current point is smaller than the current maximum point in our `k` smallest, then we replace it.
- runtime is $O(n\log(k))$ where $n$ is the number of points and $k$ is `k`.

[[heap]], [[array]], [[math]], [[priority-queue]]