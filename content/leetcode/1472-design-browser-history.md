# 1472. Design Browser History

```python
class BrowserHistory:
    def __init__(self, homepage: str):
        # most recent page is at top of stack (stack[-1])
        self.history = [homepage]
        self.idx = 0

    def visit(self, url: str) -> None:
        # pop off of self.history until we reach the page that we're on
        # push url onto stack
        while len(self.history) > (self.idx+1):
            self.history.pop()
        
        self.history.append(url)
        self.idx += 1

    def back(self, steps: int) -> str:
        # at index 0, we can go back 0 steps (can't go back)
        self.idx -= (min(steps, self.idx))
        return self.history[self.idx]

    def forward(self, steps: int) -> str:
        max_steps = len(self.history)-self.idx-1
        self.idx += min(max_steps, steps)
        return self.history[self.idx]
```

- we use a [[stack]] to keep track of history.
- use a pointer to keep track of what page we’re on.

[[lc-system-design]]