# 735. Asteroid Collision

```python
class Solution:
    def asteroidCollision(self, asteroids: List[int]) -> List[int]:
        stack = []
        i = 0
        while i < len(asteroids):
            asteroid = asteroids[i]
            if not stack:
                stack.append(asteroid)
                i += 1
                continue

            prev = stack[-1]

            # prev moving right and cur moving left
            if prev > 0 and asteroid < 0:
                if abs(prev) > abs(asteroid): # prev wins
                    i += 1
                elif abs(prev) < abs(asteroid): # cur wins
                    stack.pop()
                else: # mutual destruction
                    stack.pop()
                    i += 1
            else:
                stack.append(asteroid)
                i += 1
        return stack
```

- this is a pretty standard [[stack]] question, because we essentially just want to simulate how the asteroids will respond to each other.
	- whenever two would hit, figure out the winner and put the one that survives back into the [[stack]].

[[array]]