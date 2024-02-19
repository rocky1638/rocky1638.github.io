---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/valid-parenthesis-string/
---

# 678. Valid Parenthesis String

Given a string `s` containing only three types of characters: `'('`, `')'` and `'*'`, return `true` _if_ `s` _is **valid**_.

The following rules define a **valid** string:

- Any left parenthesis `'('` must have a corresponding right parenthesis `')'`.
- Any right parenthesis `')'` must have a corresponding left parenthesis `'('`.
- Left parenthesis `'('` must go before the corresponding right parenthesis `')'`.
- `'*'` could be treated as a single right parenthesis `')'` or a single left parenthesis `'('` or an empty string `""`.

## Backtracking with memoization.

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

- basic backtracking where we split off for each wildcard we see.
- keep track of things we’ve calculated already using a tuple of index in the string and number of unclosed opening brackets.

## Greedy.

```python
```python
class Solution:
    def checkValidString(self, s: str) -> bool:
        leftMin, leftMax = 0, 0

        for c in s:
            if c == "(":
                leftMin, leftMax = leftMin + 1, leftMax + 1
            elif c == ")":
                leftMin, leftMax = leftMin - 1, leftMax - 1
            else:
                leftMin, leftMax = leftMin - 1, leftMax + 1
            if leftMax < 0:
                return False
            if leftMin < 0:  # required because -> s = ( * ) (
                leftMin = 0
        return leftMin == 0
```

- keeping track of `leftMin` and `leftMax` allows us to store a possible range of open brackets based on whenever we see a wildcard.
- the difficult part to understand is the last `if` statement in the loop.
	- if `leftMin` ever falls below 0, we reset it back to 0 because at no point in our iteration of creating a valid string should we have a possibility of having more closing brackets than opening brackets.

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

### Video explanation.

<iframe width="560" height="315" src="https://www.youtube.com/embed/QhPdNS143Qg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[backtracking]], [[memoization]], [[greedy]], [[string]]
