---
title: 49. group anagrams
created_at: 2022-12-09
date: 2022-12-09
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/group-anagrams/
tags:
  - hashmap
  - string
  - sorting
---

Given an array of strings `strs`, group **the anagrams** together. You can return the answer in **any order**.

An **Anagram** is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

## solution

```python
class Solution:
  def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
    d = collections.defaultdict(list) 
    for s in strs:
      key = str(sorted(s))
      d[key].append(s) 
    return d.values()
```

- use a [[hashmap]] and group the strings by sorted values.
- just return the groupings at the end.
