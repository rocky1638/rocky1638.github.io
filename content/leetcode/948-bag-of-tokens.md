# 948. Bag of Tokens

```python
class Solution:
    """
    - Sort the tokens in ascending order.
    - Use two pointers moving inwards from the sides.
    - If we have enough points, we want to play the cheapest token for a score (greedily).
    - If we don't have enough points, we want to get the most value out of using a token
      for points.
    """
    def bagOfTokensScore(self, tokens: List[int], power: int) -> int:
        tokens.sort()
        score = 0
        l, r = 0, len(tokens)-1

        while l <= r:
            if power >= tokens[l]:
                score += 1
                power -= tokens[l]
                l += 1
            elif r > l and score >= 1:
                score -= 1
                power += tokens[r]
                r -= 1
            else:
                r -= 1

        return score
```

- use [[sorting]] to have the tokens in ascending order.
- use [[two-pointers]] strategy to [[greedy|greedily]] use tokens for power or for score.
	- if we can get a point by spending power, we want to spend the cheapest one first.
	- if we can’t get a point, we want to get the most possible power for sacrificing one score.
	- moving in from the left and right with [[two-pointers]] makes sense to do this.

[[array]]