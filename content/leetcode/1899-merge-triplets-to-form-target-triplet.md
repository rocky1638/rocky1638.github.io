---
created_at: 2023-01-16
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/merge-triplets-to-form-target-triplet/
---

# 1899. Merge Triplets To Form Target Triplet

A **triplet** is an array of three integers. You are given a 2D integer array `triplets`, where `triplets[i] = [ai, bi, ci]` describes the `ith` **triplet**. You are also given an integer array `target = [x, y, z]` that describes the **triplet** you want to obtain.

To obtain `target`, you may apply the following operation on `triplets` **any number** of times (possibly **zero**):

- Choose two indices (**0-indexed**) `i` and `j` (`i != j`) and **update** `triplets[j]` to become `[max(ai, aj), max(bi, bj), max(ci, cj)]`.
    - For example, if `triplets[i] = [2, 5, 3]` and `triplets[j] = [1, 7, 5]`, `triplets[j]` will be updated to `[max(2, 1), max(5, 7), max(3, 5)] = [2, 7, 5]`.

Return `true` _if it is possible to obtain the_ `target` _**triplet**_ `[x, y, z]` _as an **element** of_ `triplets`_, or_ `false` _otherwise_.

```python
class Solution:
    def mergeTriplets(self, triplets: List[List[int]], target: List[int]) -> bool:
        """
        - if a triplet has any value over the respective value in 
          target, we can't use it.
        - if a triplet has a value that equals the respective target
          value, we have that value covered.
        - if we have a triplet that satisfies each of the target values,
          we return true.
        """

        good = [False, False, False]
        for t in triplets:
            if t[0] > target[0] or t[1] > target[1] or t[2] > target[2]:
                continue
            
            for i, val in enumerate(t):
                if val == target[i]:
                    good[i] = True
        
        return all(good)
```

- we note that if a triplet has a value that’s too big for `target`, we can’t do any operations with it because we’ll overshoot the value in `target`.
- if there’s a triplet that has a value that matches the value in target, then we know we can use it along with some other value that doesn’t violate the point mentioned above.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[array]], [[greedy]]
