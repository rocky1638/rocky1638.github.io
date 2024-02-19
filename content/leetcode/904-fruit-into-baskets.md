---
created_at: 2023-01-19
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/fruit-into-baskets/
---

# 904. Fruit Into Baskets

You are visiting a farm that has a single row of fruit trees arranged from left to right. The trees are represented by an integer array `fruits` where `fruits[i]` is the **type** of fruit the `ith` tree produces.

You want to collect as much fruit as possible. However, the owner has some strict rules that you must follow:

- You only have **two** baskets, and each basket can only hold a **single type** of fruit. There is no limit on the amount of fruit each basket can hold.
- Starting from any tree of your choice, you must pick **exactly one fruit** from **every** tree (including the start tree) while moving to the right. The picked fruits must fit in one of your baskets.
- Once you reach a tree with fruit that cannot fit in your baskets, you must stop.

Given the integer array `fruits`, return _the **maximum** number of fruits you can pick_.

```python
class Solution:
    def totalFruit(self, tree):
            count, i = {}, 0
            for j, v in enumerate(tree):
                count[v] = count.get(v, 0) + 1
                if len(count) > 2:
                    count[tree[i]] -= 1
                    if count[tree[i]] == 0: del count[tree[i]]
                    i += 1
            return j - i + 1
```

- basic sliding window problem.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[sliding-window]], [[array]]
