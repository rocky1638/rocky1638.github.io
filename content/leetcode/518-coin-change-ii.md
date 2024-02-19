---
created_at: 2023-01-17
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/coin-change-ii/
---

# 518. Coin Change II

You are given an integer array `coins` representing coins of different denominations and an integer `amount` representing a total amount of money.

Return _the number of combinations that make up that amount_. If that amount of money cannot be made up by any combination of the coins, return `0`.

You may assume that you have an infinite number of each kind of coin.

The answer is **guaranteed** to fit into a signed **32-bit** integer.

## Top-down recursion with memoization.

```python
class Solution:
    def change(self, amount: int, coins: List[int]) -> int:
        ans = 0
        cache = {}

        def recurse(coin_idx, subtotal):
            if subtotal == amount:
                return 1
            if subtotal > amount:
                return 0
            if coin_idx == len(coins):
                return 0
            if (coin_idx, subtotal) in cache:
                return cache[(coin_idx, subtotal)]

            # we either use the coin (first/again), or move on.
            cache[(coin_idx, subtotal)] = recurse(coin_idx, subtotal + coins[coin_idx]) + recurse(coin_idx + 1, subtotal)
            return cache[(coin_idx, subtotal)]
        
        return recurse(0, 0)
```

- we do top-down recursion.
- at each recursive step, we can either use the current coin, or move on to the next coin.
	- we go through the coins in order so that we don’t have differently ordered repeats _(we are only looking for combinations and not permutations)_.

## 2D dynamic programming.

```python
class Solution:
    def change(self, amount: int, coins: List[int]) -> int:
        dp = [[0]*(amount+1) for _ in range(len(coins)+1)]

        for i in range(1, len(dp)):
            for j in range(len(dp[0])):
                if j == 0:
                    # one way to make 0, don't take any coins
                    dp[i][j] = 1
                else:
                    # if we don't use the current coin
                    dp[i][j] = dp[i-1][j]
                    # if we do use the current coin
                    if coins[i-1] <= j:
                        dp[i][j] += dp[i][j-coins[i-1]]

        return dp[-1][-1]
```

- we keep a dp array that has each row the length of the amount we’re trying to reach, and with number of rows equal to the coins that we’re considering.
- `dp[i][j]` represents the number of ways that we can represent the subtotal `j` using the first `i` coins.
- basically 0/1 knapsack.

## Memory optimization with 1D array.

```python
class Solution:
    def change(self, amount: int, coins: List[int]) -> int:
        dp = [0]*(amount+1)

        for i in range(1, len(coins)+1):
            nextDP = [0]*(amount+1)
            for j in range(amount+1):
                if j == 0:
                    # one way to make 0, don't take any coins
                    nextDP[j] = 1
                else:
                    # if we don't use the current coin
                    nextDP[j] = dp[j]
                    # if we do use the current coin
                    if coins[i-1] <= j:
                        nextDP[j] += nextDP[j-coins[i-1]]
            dp = nextDP

        return dp[-1]
```

- we only ever look at the previous row, so we can just store at most two rows of the dp matrix in memory at once.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[dfs]], [[recursion]], [[memoization]], [[dynamic-programming]], [[array]]
