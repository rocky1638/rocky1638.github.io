---
created_at: 2022-12-13
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/course-schedule-ii/
---

# 210. Course Schedule II

There are a total of `numCourses` courses you have to take, labeled from `0` to `numCourses - 1`. You are given an array `prerequisites` where `prerequisites[i] = [ai, bi]` indicates that you **must** take course `bi` first if you want to take course `ai`.

- For example, the pair `[0, 1]`, indicates that to take course `0` you have to first take course `1`.

Return _the ordering of courses you should take to finish all courses_. If there are many valid answers, return **any** of them. If it is impossible to finish all courses, return **an empty array**.

```python
class Solution:
    def findOrder(self, numCourses: int, prerequisites: List[List[int]]) -> List[int]:
        g = collections.defaultdict(list)
        for pre, post in prerequisites:
            g[pre].append(post)
        
        indegrees = {}
        for node in range(numCourses):
            indegrees[node] = 0
        for node in g:
            for neighbor in g[node]:
                indegrees[neighbor] += 1
        
        q = collections.deque()
        for node in range(numCourses):
            if indegrees[node] == 0:
                q.append(node)

        topsort = []
        while q:
            curnode = q.popleft()
            topsort.append(curnode)
            for neighbor in g[curnode]:
                indegrees[neighbor] -= 1
                if indegrees[neighbor] == 0:
                    q.append(neighbor)
        return topsort[::-1] if len(topsort) == numCourses else []
```

- we create a [[graph]] using an [[adjacency-list]] and perform [[topological-sort]] on it to get the valid ordering of courses.
	- we do this by finding all the nodes with an indegree of zero, and then performing [[bfs]], updating our indegrees everytime we’re finished with a node, and adding new nodes that now have an indegree of zero.

## Related.

- [[207-course-schedule]].

Categories:: [[graph]], [[adjacency-list]], [[topological-sort]], [[bfs]]