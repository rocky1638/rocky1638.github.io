---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/partition-labels/
---

# 763. Partition Labels

You are given a string `s`. We want to partition the string into as many parts as possible so that each letter appears in at most one part.

Note that the partition is done so that after concatenating all the parts in order, the resultant string should be `s`.

Return _a list of integers representing the size of these parts_.

```python
class Solution:
    def partitionLabels(self, s: str) -> List[int]:
        """
        - keep a hashmap of the earliest index that each char appears.
        - greedily, we want to strive for each letter
          being in its own partition.
        - when we see a repeat, all the letters between new and old char
          have their leftmost idx set to the leftmost of this repeated char.
            - O(26)
        """

        h = {}
        starts = set()

        for i, char in enumerate(s):
            # first time seeing this char
            if char not in h:
                h[char] = i
                starts.add(i)
            else:
                for key in h:
                    if h[key] > h[char]:
                        if h[key] in starts:    
                            starts.remove(h[key])
                        h[key] = h[char]

        starts = list(starts) + [len(s)]
        starts.sort()
        ans = []
        for i in range(1, len(starts)):
            ans.append(starts[i]-starts[i-1])
            i += 1
        return ans
```

- we iterate through the string, and store the first occurence of each character.
	- if we see the character again, then any character that we saw in between now also belongs to that partition, and we set those characters’ start indices to the same value as the repeated char.
- at the end, we do some manipulation to return the format that leetcode accepts.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[greedy]], [[hashmap]], [[sorting]], [[string]]
