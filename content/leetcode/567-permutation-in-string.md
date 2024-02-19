---
created_at: 2023-01-05
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/permutation-in-string/
---

# 567. Permutation In String

Given two strings `s1` and `s2`, return `true` _if_ `s2` _contains a permutation of_ `s1`_, or_ `false` _otherwise_.

In other words, return `true` if one of `s1`'s permutations is the substring of `s2`.

## Recalculate frequency with each iteration.

```python
class Solution:
    def checkInclusion(self, s1: str, s2: str) -> bool:
        s1c = collections.Counter(s1)
        s2c = collections.Counter(s2)

        l, r = 0, len(s1)-1

        while r < len(s2):
            consideration = collections.Counter(s2[l:r+1])

            if consideration == s1c:
                return True
            
            l += 1
            r += 1

        return False
```

- use two frequency map objects and a fixed-size sliding window to check if any of the sliding windows have the correct frequency of letters.

## Optimization to incrementally update frequency map.

```python
class Solution:
    def checkInclusion(self, s1: str, s2: str) -> bool:
        s1c = collections.Counter(s1)

        consideration = collections.Counter(s2[:len(s1)])
        l, r = 0, len(s1)-1

        while r < len(s2):
            if consideration == s1c:
                return True
            
            consideration[s2[l]] -= 1
            l += 1
            r += 1
            if r < len(s2):
                consideration[s2[r]] += 1

        return False
```

- only edit the frequency counter for things that change in the window instead of recalculating the whole thing every time.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[sliding-window]], [[frequency-map]], [[hashmap]], [[string]]
