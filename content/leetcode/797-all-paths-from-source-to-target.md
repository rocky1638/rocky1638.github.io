# 797. All Paths From Source to Target

```python
class Solution:
    def allPathsSourceTarget(self, graph: List[List[int]]) -> List[List[int]]:
        ans = []
        path = []
        
        def dfs(node):
            if node == (len(graph)-1):
                ans.append(path[:])
            else:
                for neighbor in graph[node]:
                    path.append(neighbor)
                    dfs(neighbor)
                    path.pop()
                    
        # dfs from node 0
        path.append(0)
        dfs(0)
        
        # return answer
        return ans
```

- a simple [[dfs]] traversal of the [[graph]] to find all the paths.

[[backtracking]]