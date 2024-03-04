---
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/valid-parenthesis-string/
tags:
  - greedy
  - memoization
date: 2023-01-17
updated: 2024-03-02
---

Given a string `s` containing only three types of characters: `'('`, `')'` and `'*'`, return `true` _if_ `s` _is **valid**_.

The following rules define a **valid** string:

- Any left parenthesis `'('` must have a corresponding right parenthesis `')'`.
- Any right parenthesis `')'` must have a corresponding left parenthesis `'('`.
- Left parenthesis `'('` must go before the corresponding right parenthesis `')'`.
- `'*'` could be treated as a single right parenthesis `')'` or a single left parenthesis `'('` or an empty string `""`.

## solution

### backtracking with memoization

The logical first step when reading this problem is to imagine the possibility of exploring every possibility when we see a wildcard, which is recursing with one of each in `["(", ")", " "]`.

This unfortunately is $O(3^n)$ in the worst case.

However, we can memoize these recursive calls by the two values we care about (our index in the array, `idx`, and the number of unclosed left brackets, `num_left`).

```python
class Solution:
	def checkValidString(self, s: str) -> bool:
		memo = {(len(s), 0): True}
			def dfs(idx, num_left):
				if idx == len(s) or num_left < 0:
					return num_left == 0
				if (idx, num_left) in memo:
					return memo[(idx, num_left)]

				if s[idx] == "(":
					memo[(idx, num_left)] = dfs(idx+1, num_left+1)
				elif s[idx] == ")":
					memo[(idx, num_left)] = dfs(idx+1, num_left-1)
				else:
					memo[(idx, num_left)] = dfs(idx+1, num_left+1) or dfs(idx+1, num_left-1) or dfs(idx+1, num_left)
				return memo[(idx, num_left)]

			return dfs(0, 0)
```

### greedy

To get a better $O(n)$ solution, we have to do something that’s pretty hard to come up with on your own.

First, note that if we didn’t have wildcards, we could just keep a simple count of how many unclosed left brackets we had at any time as we iterated through the string.

If this number, `left` dropped below 0 at any point (e.g. on a string like `"(()))"`), or if we ended with `left > 0` (e.g. on a string like `"())"`), then we would return false.

However, with wildcards, this number of open left brackets diverges into a range of possibilities.

The key insight is to realize we can store both the minimum and maximum possible number of open left brackets at any time, and that each of these values helps us determine one of the failure modes described above. Namely:

1. If the maximum possible number of open left brackets `maxLeft` drops below 0, that means that even by setting all `* = (`, we still had too many right brackets.
2. If the minimum possible number of open left brackets is not equal to 0 by the end of our string, that means that even with all wildcards being used to close left brackets when they can, we still have leftover unclosed left brackets (e.g. `"(*())("`)

```python
def checkValidString(self, s: str):
	# store the number of currently unclosed
	# left brackets
	# because of wildcards, we maintain a min
	# and max value.
	minLeft, maxLeft = 0, 0
	
	for c in s:
		if c == "(":
			minLeft += 1
			maxLeft += 1
		elif c == ")":
			minLeft -= 1
			maxLeft -= 1
		elif c == "*":
			minLeft -= 1 # if we choose * = )
			maxLeft += 1 # if we choose * = (
		
		# even with wildcards all being
		# (, we weren't able to keep enough
		# opening brackets
		if maxLeft < 0:
			return False
	
		# this only happens because we
		# set a * to ). Instead, we can just
		# set that prior * to an empty string.
		if minLeft < 0:
			minLeft = 0
	
	return minLeft == 0
```

#### explanation of resetting `minLeft` to 0

```
walking through ( * ) (

(: leftMin = 1, leftMax = 1
(*: leftMin = 0, leftMax = 2

- here, when leftMin is -1, it is representing the
  prospective string "())" which is invalid.
- instead we can set leftMin to 0, representing if
  we had chosen for the wildcard to be a space.
  
(*): leftMin = -1, leftMax = 1
     leftMin = 0, leftMax = 1
	 
(*)(: leftMin = 1, leftMax = 2

-> return False
```

## references.

- https://www.youtube.com/embed/QhPdNS143Qg
