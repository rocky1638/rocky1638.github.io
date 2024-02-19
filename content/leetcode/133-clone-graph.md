---
created_at: 2022-11-19
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/clone-graph/
---

# 133. Clone Graph

```python
class Solution:
    def cloneGraph(self, node: 'Node') -> 'Nodxe':
        if not node:
            return None
        
        clones = {}
        visited = set([node.val])
        
        ret = Node(node.val)
        clones[node.val] = ret
        q = deque([node])
         
        while q:
            cur = q.popleft()
            cur_clone = clones[cur.val]
            
            for n in cur.neighbors:
                # clone neighbor node
                n_clone = None
                if n.val in clones:
                    n_clone = clones[n.val]
                else:
                    n_clone = Node(n.val)
                    clones[n.val] = n_clone

                # link the two new nodes
                cur_clone.neighbors.append(n_clone)
                
                if n.val not in visited:
                    # append neighbor to queue
                    q.append(n)
                    # add to visited
                    visited.add(n.val)
        
        return ret
```

- conduct a normal [[bfs]] or [[dfs]] to reach all the nodes.
- we want to visit every node in order to link the correct cloned nodes’ neighbors, so the behavior of the `visited` set is slightly different than in a normal [[bfs]].
- keep track of cloned nodes in a [[hashmap]].

Categories:: [[bfs]], [[dfs]], [[hashmap]], [[graph]]
