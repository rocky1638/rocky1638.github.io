---
created_at: 2023-01-16
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/minimum-interval-to-include-each-query/
---

# 1851. Minimum Interval To Include Each Query

<iframe width="560" height="315" src="https://www.youtube.com/embed/5hQ5WWW5awQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Neetcode notes.

- [00:05](https://www.youtube.com/watch?v=5hQ5WWW5awQ#t=5.882038881744385) problem walkthrough and description.
- [03:03](https://www.youtube.com/watch?v=5hQ5WWW5awQ#t=183.3793439408722) brute force solution.
	- for every query, just scan every interval.
	- $O(mn)$.
- [05:00](https://www.youtube.com/watch?v=5hQ5WWW5awQ#t=300.96186803433227) walkthrough of optimal solution.
	- we sort the intervals and the queries.
	- go through the intervals until the start value is past the query, when we can stop early.
	- we keep a min heap of lengths of the intervals that satisfy a query, as well as the end position of each of these intervals.
		- we keep track of the end of the interval to make sure to lazy delete these intervals from the heap if our query starts after the end time of the interval.

```python
class Solution:
    def minInterval(self, intervals: List[List[int]], queries: List[int]) -> List[int]:
        """
        Brute Force:
        - for each query, we could iterate through all the ranges and
          keep track of the smallest one.
        - O(mn)
        Optimizations:
        - if we sort the intervals, we can stop early when the start
          of the interval is bigger than the query.
        - we can also sort the queries
        - then, we can use a min heap to store the sizes of the interval,
          as well as the end times for each interval.
        - go through the queries, and enheap all of the intervals that
          contain the query.
            - grab the smallest one and output it to the answer array.
        - lazy delete heap entries that no longer work for the current query.
        """

        intervals.sort(key=lambda x: x[0])
        queries_with_idx = [(q, idx) for idx, q in enumerate(queries)]
        queries_with_idx.sort(key=lambda x: x[0])

        h = []
        int_idx = 0 
        ans = [-1]*len(queries)
        for query, idx in queries_with_idx:
            while int_idx < len(intervals):
                start, end = intervals[int_idx][0], intervals[int_idx][1]
                # if query falls into interval, enheap it.
                if start <= query and end >= query:
                    heapq.heappush(h, (end-start+1, end))
                    int_idx += 1
                # none of our queries care about this interval.
                elif end < query:
                    int_idx += 1
                else:
                    break

            # keep popping until we find the smallest valid interval.
            while h:
                size, end = h[0]
                if end >= query:
                    ans[idx] = size
                    break
                # we are lazily deleting old intervals
                # here that are no longer valid.
                else:
                    heapq.heappop(h)

        return ans
```

- an intuition is that if we sort the intervals and queries, then we can “stop early” once an interval’s end is smaller than the query we’re currently looking at.
	- also that if an interval starts after our query, we don’t have to consider it yet.
- for this ongoing sorted behavior, we use a heap.
- we make use of lazy deletion in the heap.
	- we do this by keeping track of the end time for each interval, so if it’s still on the heap when our query is already past it, we know to not consider it and just pop it.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

- https://www.youtube.com/watch?v=5hQ5WWW5awQ

Categories:: [[interval]], [[heap]], [[sorting]], [[array]]
