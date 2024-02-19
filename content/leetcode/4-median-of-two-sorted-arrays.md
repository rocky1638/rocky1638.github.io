---
created_at: 2023-01-02
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/median-of-two-sorted-arrays/
---

# 4. Median Of Two Sorted Arrays

```python
class Solution:
    def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
        a, b = nums1, nums2
        total = len(a) + len(b)
        half = total // 2

        # a is always the shorter array
        if len(b) < len(a):
            a, b = b, a
        
        l, r = 0, len(a) - 1
        while True:
            ma = (l+r) // 2 # middle index for a
            mb = half - ma - 2 # middle index for b

            aleft = a[ma] if ma >= 0 else float("-infinity")
            aright = a[ma+1] if ma+1 < len(a) else float("infinity")
            bleft = b[mb] if mb >= 0 else float("-infinity")
            bright = b[mb+1] if mb+1 < len(b) else float("infinity")

            # partition is correct
            if aleft <= bright and bleft <= aright:
                if total % 2 == 0:
                    return (max(aleft, bleft) + min(aright, bright)) / 2
                else:
                    return min(aright, bright)

            elif aleft > bright:
                r = ma - 1
            else: # aright < bleft
                l = ma + 1
```

## Neetcode video notes.

- [02:32](https://www.youtube.com/watch?v=q6IEA26hvXc#t=152.54057795422364) the actual logical definition of a median.
- [03:16](https://www.youtube.com/watch?v=q6IEA26hvXc#t=196.84639202098083) we essentially want to simulate looking through a merged array without actually merging them.
	- we want to partition the array into valid left and right halfs, because then the median will just be in the middle.
- [08:27](https://www.youtube.com/watch?v=q6IEA26hvXc#t=507.3298399103546) how to partition into left and right partitions without merging.
- [10:34](https://www.youtube.com/watch?v=q6IEA26hvXc#t=634.1080160095368) once we partition one of the arrays, we know the size that the partition should be in the other array because the total size of the partition should be `(len(a)+len(b)) // 2`.
- [13:14](https://www.youtube.com/watch?v=q6IEA26hvXc#t=794.7069969904633) edge cases for when we don’t include either of the arrays in our partition.
- [14:08](https://www.youtube.com/watch?v=q6IEA26hvXc#t=848.4556927108475) code walkthrough.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

- https://www.youtube.com/watch?v=q6IEA26hvXc

Categories:: [[binary-search]], [[divide-and-conquer]], [[array]]
