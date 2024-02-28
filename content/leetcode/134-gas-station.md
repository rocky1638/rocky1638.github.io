---
title: 134. gas station
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/gas-station/
date: 2022-12-09
updated: 2024-02-28
tags:
  - greedy
  - array
---

There are `n` gas stations along a circular route, where the amount of gas at the `ith` station is `gas[i]`.

You have a car with an unlimited gas tank and it costs `cost[i]` of gas to travel from the `ith` station to its next `(i + 1)th` station. You begin the journey with an empty tank at one of the gas stations.

Given two integer arrays `gas` and `cost`, return _the starting gas station's index if you can travel around the circuit once in the clockwise direction, otherwise return_ `-1`. If there exists a solution, it is **guaranteed** to be **unique**.

## solution

Consider the example below:

![[134-gas-station-example.png]]

Our first thought is to check each station as a starting point in clockwise order, and then return the one that allows us to go the whole way around the loop. However, this takes $O(n^2)$ time.

The key observation is that there is repeated work in the calculation above. See the example below:

![[134-gas-station-greedy.png]]

We start at index 0 with an initial gas tank of 0, and then fill up with the 7 gas available at the station. We manage to make it to index 1, but can only reach index 2 with a negative gas tank.

The brute force solution would have us start our search over at index 1, but we can prove that there is no need to search this station.

Consider the general case in which our car manages to travel between stations $i$ and $j$, but reaches a negative gas tank at index $j+1$.

When we travelled from station $i$ to $i+1$, we carried over an amount of gas $g$ such that

$$
g \in [0,\infty)
$$

Now, if we were to brute-force and start our simulation again at $i+1$, we know for sure that we are starting with 0 gas, which is $\leq g$.

Therefore, starting at index $i+1$ is **equal or worse** to starting at index $i$. By induction, we conclude that all starting points $x \in [i,j]$ are equal-to or worse than starting point $i$.

As such, we should just continue our search at index $j+1$.

```python
class Solution:
	def canCompleteCircuit(self, gas: List[int], cost: List[int]) -> int:
		if sum(cost) > sum(gas):
			return -1
	
		tank = 0
		cur_idx = 0
		start = 0
	
		for i in range(len(gas)):
			# if our tank went negative, reset
			# and start search anew from here
			if tank < 0:
				tank = 0
				start = i
			
			tank += gas[cur_idx]
			tank -= cost[cur_idx]
			cur_idx += 1
		
		return start
```
