---
title: 48. rotate image
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/rotate-image/
date: 2022-12-27
updated: 2024-03-22
tags:
  - array
---

Literally just matrix logic. We keep four pointers starting on each corner of each layer, and move our pointers along the sides.

```python
def rotate(self, matrix: List[List[int]]) -> None:
	"""
	Do not return anything, modify matrix in-place instead.
	"""
	n = len(matrix)
	its = n // 2
	
	for it in range(its):
		tl = [0 + it, 0 + it]
		tr = [0 + it, n - 1 - it]
		bl = [n - 1 - it, 0 + it]
		br = [n - 1 - it, n - 1 - it]
		
		for _ in range(n-1-(2*it)):
			tr_temp = matrix[tr[0]][tr[1]]
			matrix[tr[0]][tr[1]] = matrix[tl[0]][tl[1]]
			matrix[tl[0]][tl[1]] = matrix[bl[0]][bl[1]]
			matrix[bl[0]][bl[1]] = matrix[br[0]][br[1]]
			matrix[br[0]][br[1]] = tr_temp
			
			tl[1] += 1
			tr[0] += 1
			br[1] -= 1 
			bl[0] -= 1
```
