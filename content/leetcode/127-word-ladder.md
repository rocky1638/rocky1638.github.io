---
created_at: 2022-11-25
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/word-ladder/
---

# 127. Word Ladder

```python
class Solution:
    def ladderLength(self, beginWord: str, endWord: str, wordList: List[str]) -> int:
        # make a graph where connections go between words that are one change apart
        # bfs to find shortest path between beginWord and endWord
        
        def isNeighbor(w1, w2):
            num_diffs = 0
            
            for c1, c2 in zip(w1, w2):
                if c1 != c2:
                    num_diffs += 1
                    if num_diffs > 1:
                        return False
            return num_diffs == 1
        
        # make the graph
        g = defaultdict(list)
        
        wordList = [beginWord] + wordList
        
        for word in wordList:
            for i in range(len(beginWord)):
                g[word[:i] + "_" + word[i+1:]].append(word)

        # bfs
        q = deque([beginWord])
        level = 1
        seen = set([beginWord])
        
        while q:
            level_len = len(q)
            
            for _ in range(level_len):
                cur = q.popleft()
                
                if cur == endWord:
                    return level
                
                for i in range(len(cur)):
                    intermediate_word = cur[:i] + "_" + cur[i+1:]
                    
                    for neighbor in g[intermediate_word]:
                        if neighbor not in seen:
                            q.append(neighbor)
                            seen.add(neighbor)
            
            level += 1
        return 0
```

- the approach is pretty straightforward, by creating a [[graph]] that links words that are one character apart from each other, and then performing [[bfs]] to find the shortest path between `beginWord` and `endWord`.
- the hard part is creating the graph in better than $O(n^2)$ time, because that times out.
- the key is to not directly link all the words together, but store each *intermediate step* as a key in the [[hashmap]], where each word that can reach that intermediate step is added to the array at that key.

![[127-e1.excalidraw]]

- then, when we [[bfs]], we can just go through each possible intermediate step for the current node, and look at all the neighbors that also share this intermediate step.

Categories:: [[hashmap]], [[bfs]], [[graph]], [[string]]
