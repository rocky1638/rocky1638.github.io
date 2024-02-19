---
created_at: 2022-11-17
type: leetcode
aliases: []
difficulty: 🔴
link: https://leetcode.com/problems/word-break-ii/
---

# 140. Word Break II

## Memoization using `@lru_cache`.

```python
class Solution:
    def wordBreak(self, s: str, wordDict: List[str]) -> List[str]:
        wordSet = set(wordDict)
        ans = []
        
        @lru_cache
        def recurse(i, acc):
            nonlocal ans

            if i == len(s):
                ans.append(acc)
                return
            
            string = ""
            while i < len(s):
                string += s[i]
                if string in wordSet:
                    if len(acc) == 0:
                        recurse(i+1, string)
                    else:
                        recurse(i+1, acc+" "+string)
                i += 1
        
        recurse(0, "")
        return ans
```

- we can use a top down recursive approach to find all the possibilities.
- this is pretty intuitive and straightforward.
- we optimize by memoizing repeated recursive calls.

## Memoization using custom hashmap.

```python
class Solution:
    def wordBreak(self, s: str, wordDict: List[str]) -> List[str]:
        wordSet = set(wordDict)
        ans = []
        memo = defaultdict()
        
        def recurse(i, acc):
            nonlocal ans

            if i == len(s):
                ans.append(acc)
                return
            
            if f"{i}{acc}" in memo:
                recurse(memo[f"{i}{string}"][0], memo[f"{i}{acc}"][1])
            else:
                string = ""
                while i < len(s):
                    string += s[i]
                    if string in wordSet:
                        if len(acc) == 0:
                            memo[f"{i}{acc}"] = [i+1, string]
                            recurse(i+1, string)
                        else:
                            memo[f"{i}{acc}"] = [i+1, acc+" "+string]
                            recurse(i+1, acc+" "+string)
                    i += 1
        
        recurse(0, "")
        return ans
```

Categories:: [[recursion]], [[backtracking]], [[memoization]]
