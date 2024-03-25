---
title: 127. word ladder
type: leetcode
aliases: 
difficulty: 🔴
link: https://leetcode.com/problems/word-ladder/
date: 2022-11-25
updated: 2024-03-24
tags:
  - bfs
  - graph
---

A **transformation sequence** from word `beginWord` to word `endWord` using a dictionary `wordList` is a sequence of words `beginWord -> s1 -> s2 -> ... -> sk` such that:

- Every adjacent pair of words differs by a single letter.
- Every `si` for `1 <= i <= k` is in `wordList`. Note that `beginWord` does not need to be in `wordList`.
- `sk == endWord`

Given two words, `beginWord` and `endWord`, and a dictionary `wordList`, return _the **number of words** in the **shortest transformation sequence** from_ `beginWord` _to_ `endWord`_, or_ `0` _if no such sequence exists._

## solution

The approach is pretty straightforward, by creating a [[graph]] that links words that are one character apart from each other, and then performing [[bfs]] to find the shortest path between `beginWord` and `endWord`.

The hard part is creating the graph in better than $O(n^2)$ time, because that times out. The key is to not directly link all the words together, but store each _intermediate step_ as a key in the [[hashmap]], where each word that can reach that intermediate step is added to the array at that key.

![[127-e1.excalidraw]]

Then, when we breadth-first search, we can just go through each possible intermediate step for the current node, and look at all the neighbors that also share this intermediate step.

```python
def ladderLength(self, beginWord: str, endWord: str, wordList: List[str]) -> int:
	g = defaultdict(list)
	
	for word in wordList:
		for i in range(len(word)):
			key = word[:i] + "_" + word[i+1:]
			g[key].append(word)
	
	q = deque([beginWord])
	visited = set()
	depth = 1
	
	while q:
		level_len = len(q)
		for i in range(level_len):
			cur_word = q.pop()
		
		if cur_word == endWord:
			return depth
		
		neighbors = []
		for i in range(len(cur_word)):
			key = cur_word[:i] + "_" + cur_word[i+1:]
			neighbors += g[key]
		
		for n in neighbors:
			if n not in visited:
				visited.add(n)
				q.appendleft(n)
				
		depth += 1
	
	return 0
```
