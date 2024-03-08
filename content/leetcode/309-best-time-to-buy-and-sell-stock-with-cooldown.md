---
type: leetcode
title: "309: best time to buy and sell stock with cooldown"
tags:
aliases: 
parents: 
children: 
supports: 
enemies:
date: 2022-12-30
updated: 2024-03-07
---

You are given an array `prices` where `prices[i]` is the price of a given stock on the `ith` day.

Find the maximum profit you can achieve. You may complete as many transactions as you like (i.e., buy one and sell one share of the stock multiple times) with the following restrictions:

- After you sell your stock, you cannot buy stock on the next day (i.e., cooldown one day).

**Note:** You may not engage in multiple transactions simultaneously (i.e., you must sell the stock before you buy again).

## solutions

### top-down dfs with memoization

```python
def maxProfit(self, prices: List[int]) -> int:
	@cache
	def dp(i, holding, cooldown):
		if i == len(prices):
			return 0
		if cooldown:
			return dp(i + 1, False, False)
		if holding:
			return max( prices[i] + dp(i + 1, False, True), # sell
			dp(i + 1, True, False) # hold
		)
		return max(
			-prices[i] + dp(i + 1, True, False), # buy
			dp(i + 1, False, False) # skip
		)

	return dp(0, False, False)
```

### bottom-up dp in $O(n^2)$

Why is this solution not able to solve the question in $O(n)$? What key piece of information am I not taking advantage of?

I think the issue is that because I’m only storing the three rows of DP by the action taken on the day, and not by something more actionable like “am I holding a stock?”, when I go to calculate the “sell” value for a day, I need to check all days because I can’t just look at a built-up cache of “max profit if the last action was a buy, and I am currently holding stock”.

If I build up a value of “max profit if the last action was a buy (i.e. we are now holding a stock)”, I can safely assume that any previous trades made were optimal before this current buy — formally, say that if we have a val

If anyone has any clear explanation for this, please reach out to me.

```python
def maxProfit(self, prices: List[int]) -> int:
	dp = [[0] * len(prices) for _ in range(3)]
	
	for i in range(1, len(prices)):
		# buy
		if i == 1:
			# b[i] = w[i-1]
			dp[0][i] = dp[1][i-1]
		else:
			# b[i] = max(w[i-1], s[i-2])
			dp[0][i] = max(dp[1][i-2], dp[2][i-1])

		# sell
		best = 0
		for j in range(i):
			best = max(best, prices[i] - prices[j] + dp[0][j])
		dp[1][i] = best

		# wait
		dp[2][i] = max(dp[0][i-1], dp[1][i-1], dp[2][i-1])

	return max([row[-1] for row in dp])
```

### bottom-up dp in $O(n)$

The only reason we need the third “just sold” state is to encode the rule that we can’t immediately buy after selling. If that rule wasn’t there, we could just simply have two states of “holding a stock” and “not holding a stock”.

```python
def maxProfit(self, prices: List[int]) -> int:
	"""
	three states:
	- not holding stock (sold in the past and haven't bought a new stock yet/ever)
	- holding stock (bought today or in past)
	- just sold stock (must have rested yesterday)
	"""
	
	not_holding, holding, sold = 0, -prices[0], 0
	
	for price in prices[1:]:
		prev_not_holding, prev_holding, prev_sold = not_holding, holding, sold
	
		# not holding
		# we either just sold yesterday, or were also not holding yesterday
		not_holding = max(prev_not_holding, prev_sold)
		
		# holding
		# we either just bought, or were also holding yesterday
		holding = max(prev_holding, prev_not_holding - price)
		
		# sold
		# we just sold, so we must have rested yesterday
		sold = prev_holding + price
	
	return max(not_holding, holding, sold)
```
