# 1583. Count Unhappy Friends

```python
class Solution:
    def unhappyFriends(self, n: int, preferences: List[List[int]], pairs: List[List[int]]) -> int:
        ans = 0
        
        # store pairs in dict for easy lookup
        pd = defaultdict()
        for f1, f2 in pairs:
            pd[f1] = f2
            pd[f2] = f1
        
        # build rank matrix where mat[i][j] is the rank that i holds j
        # lower rank is better friend
        mat = [[0 for _ in range(n)] for _ in range(n)]
        for i, preference in enumerate(preferences):
            rank = 1
            for friend in preference:
                mat[i][friend] = rank
                rank += 1
        
        for f1 in range(n):
            f2 = pd[f1]
            i = 0
            while i < len(preferences[f1]) and preferences[f1][i] != f2:
                other_f1 = preferences[f1][i]
                other_f1_friend = pd[other_f1]
                # other_f1 has to prefer f1 over other_f1_friend
                # for their to be an unhappy pair
                if mat[other_f1][f1] < mat[other_f1][other_f1_friend]:
                    ans += 1
                    break
                else:
                    i += 1
        return ans
```

- the hardest part here is figuring out how we efficiently look up whether someone prefers one friend over another, without having to iterate through the person’s preference [[array]] in $O(n)$ time.
	- as usual, we can make a memory vs. time tradeoff and create a two-dimensional [[matrix]] where `matrix[i][j]` represents the ranking of person `j` in the eyes of person `i`.
	- this allows us to compare preferences in $O(1)$ time.
- i created a [[hashmap]] of the pairings for easier lookup.