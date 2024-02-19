# 1244. Design A Leaderboard

```python
class Leaderboard:

    def __init__(self):
        self.d = defaultdict(int)

    def addScore(self, playerId: int, score: int) -> None:
        self.d[playerId] += score

    def top(self, K: int) -> int:
        return sum(sorted(list(self.d.values()), reverse=True)[:K])

    def reset(self, playerId: int) -> None:
        del self.d[playerId]
```

- we just keep a [[hashmap]] of all the scores and sort the top values when `top()` is called.
- prefer this over a heap because scores can be added too.

[[sorting]], [[lc-system-design]]