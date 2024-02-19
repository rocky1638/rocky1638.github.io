---
created_at: 2023-01-18
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/number-of-dice-rolls-with-target-sum/
---

# 1155. Number Of Dice Rolls With Target Sum

You have `n` dice, and each die has `k` faces numbered from `1` to `k`.

Given three integers `n`, `k`, and `target`, return _the number of possible ways (out of the_ `k^n` _total ways)_ _to roll the dice, so the sum of the face-up numbers equals_ `target`. Since the answer may be too large, return it **modulo** `10^9 + 7`.

## Top-down recursion with memoization.

```python
class Solution:
    def numRollsToTarget(self, n: int, k: int, target: int) -> int:
        """
        - backtracking with memoization -> dynamic programming approach.
        - brute force.
            - work our way up to n dice, choosing each value from 1-k for 
              each dice roll.
        """
        memo = {}
        
        def recurse(num_dice, subtotal):
            # already cached
            if (num_dice, subtotal) in memo:
                return memo[(num_dice, subtotal)]
            # positive base case
            if num_dice == n and subtotal == target:
                return 1
            
            # negative base cases
            if num_dice > n:
                return 0
            if subtotal > target: # can't have negative roll
                return 0
            
            memo[(num_dice, subtotal)] = 0
            for roll in range(1, k+1):
                memo[(num_dice, subtotal)] += recurse(num_dice + 1, subtotal + roll)
            return memo[(num_dice, subtotal)]
        
        return recurse(0, 0) % (10**9+7)
```

- simple top-down recursion with memoization.

## 2D dynamic programming.

```python
class Solution:
    def numRollsToTarget(self, n: int, k: int, target: int) -> int:
        """
        - 2d DP.
        - dp[i][j] represents the number of ways to roll to j using
          the first i dice.
        - row has length of target+1.
        - column has length of n+1.
        """

        dp = [0]*(target+1)
        # one way to make 0 target with 0 dice.
        dp[0] = 1

        for i in range(n):
            newDP = [0]*(target+1)
            for j in range(1, target+1):
                for roll in range(1, k+1):
                    if j >= roll:
                        newDP[j] += dp[j-roll]
                        newDP[j] %= 10**9+7
                    else: break
            dp = newDP
        return dp[-1]
```

- similar to coin change or knapsack.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[recursion]], [[memoization]], [[backtracking]], [[dynamic-programming]]
