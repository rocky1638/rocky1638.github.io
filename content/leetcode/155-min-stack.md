---
created_at: 2022-11-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/min-stack/
---

# 155. Min Stack

```python
class MinStack:
    """
    Every time we push a value onto the stack, we also record the current minimum.
    """
    def __init__(self):
        # stack[i] = (val at i, minimum of stack up to and including i)
        self.stack = []

    def push(self, val: int) -> None:
        if not self.stack:
            self.stack.append((val, val))
        else:
            curmin = self.stack[-1][1]
            self.stack.append((val, min(curmin, val)))

    def pop(self) -> None:
        self.stack.pop()
        
    def top(self) -> int:
        return self.stack[-1][0]

    def getMin(self) -> int:
        return self.stack[-1][1]
```

- once again, we use more data to save on time complexity.
- every time we push into the stack, we also push in the minimum value of the stack **up to and including the current value**.

![[155-e1.excalidraw]]
- then, if we pop the value that is the current minimum, we know that the next minimum is the value stored in the top of the stack at the `[1]` index.

Categories:: [[stack]], [[lc-system-design]]
