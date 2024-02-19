---
created_at: 2022-11-25
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/find-median-from-data-stream/
---

# 295. Find Median From Data Stream

The **median** is the middle value in an ordered integer list. If the size of the list is even, there is no middle value, and the median is the mean of the two middle values.

- For example, for `arr = [2,3,4]`, the median is `3`.
- For example, for `arr = [2,3]`, the median is `(2 + 3) / 2 = 2.5`.

Implement the MedianFinder class:

- `MedianFinder()` initializes the `MedianFinder` object.
- `void addNum(int num)` adds the integer `num` from the data stream to the data structure.
- `double findMedian()` returns the median of all elements so far. Answers within `10-5` of the actual answer will be accepted.

## Using binary search.

```python
class MedianFinder:

    def __init__(self):
        self.a = []

    def addNum(self, num: int) -> None:
        lo, hi = 0, len(self.a)
        while lo < hi:
            mid = (lo + hi) // 2
            if self.a[mid] < num:
                lo = mid + 1
            else:
                hi = mid
        self.a.insert(lo, num)
        
        # can also just do this
        # bisect.insort(self.a, num)

    def findMedian(self) -> float:
        if len(self.a) % 2 == 0:
            return (self.a[len(self.a)//2-1] + self.a[len(self.a)//2]) / 2
        else:
            return self.a[len(self.a)//2]
```

- we keep a sorted array, and insert new values using [[binary-search]].
- we can initialize `hi` at `len(self.a)` because we only ever use `lo` when doing the actual `insert` call.
- although we do find the position in $O(\log n)$ time, the `insert` call is linear.

## Using two heaps.

```python
from heapq import *

class MedianFinder:
    """
    we want to maintain the invariant where the left half
    is always equal or one less length than the right half.
    """
    def __init__(self):
        self.small = []  # the smaller half of the list, max heap (invert min-heap)
        self.large = []  # the larger half of the list, min heap

    def addNum(self, num):
        if len(self.small) == len(self.large):
            """
            we want to end up with lengths k, k+1
            to maintain the property that everything in the
            left half is smaller than right, we first push the new value
            into the left half, then move the largest value from the left
            to the right.
            """
            heappush(self.large, -heappushpop(self.small, -num))
        else:
            """
            we want to end with equal lengths of both halves.
            to maintain the same property described above, we first push
            the new value into the right, then move the smallest value
            in the right half to the left.
            """
            heappush(self.small, -heappushpop(self.large, num))

    def findMedian(self):
        if len(self.small) == len(self.large):
            return float(self.large[0] - self.small[0]) / 2.0
        else:
            return float(self.large[0])
```

- we maintain two heaps, where the left one is a max heap and the right one is a min heap.
	- all values in the left heap are smaller or equal than the values in the right heap.
		- we have to first push into the heap we want to move a value from and reheap, in order to maintain this invariant when inserting a new number and trying to maintain the lengths of both heaps.
	- the median is always in the “middle” of these two heaps.
- maintain lengths such that the right heap is always equal length, or one longer than the left heap.

Categories:: [[array]], [[binary-search]], [[heap]]
