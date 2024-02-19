---
created_at: 2023-01-11
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/palindrome-partitioning/
---

# 131. Palindrome Partitioning

Given a string `s`, partition `s` such that every substring of the partition is a **palindrome**. Return _all possible palindrome partitioning of_ `s`.

```python
class Solution:
    def partition(self, s: str) -> List[List[str]]:
        ans = []

		"""
        find all partitions that start at some index
        h[starting_idx] = [end_idx, end_idx]
        O(n^2)
		"""
        h = collections.defaultdict(set)

        def expandOutward(l, r):
            while l >= 0 and r < len(s):
                if s[l] == s[r]:
                    h[l].add(r)
                    l -= 1
                    r += 1
                else:
                    break

        for idx in range(len(s)):
            h[idx].add(idx)

            # check palindromes of odd length
            expandOutward(idx-1, idx+1)
            # check palindromes of even length
            expandOutward(idx, idx+1)


		"""
		Backtracking
		"""
        def recurse(acc, idx):
            if idx == len(s):
                ans.append(acc)
            else:
                for ending_idx in list(h[idx]):
                    recurse(acc[:]+[s[idx:ending_idx+1]], ending_idx+1)
                
        recurse([], 0)
        return ans
```

- we first create a precalculated hashmap that contains the indexes that palindromes end at, starting at each index.
- then, we just backtrack and get all the possible splits.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[recursion]], [[string]], [[two-pointers]], [[backtracking]], [[array]]
