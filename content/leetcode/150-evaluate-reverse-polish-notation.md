---
created_at: 2022-11-20
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/evaluate-reverse-polish-notation/
---

# 150. Evaluate Reverse Polish Notation

```python
class Solution:
    def evalRPN(self, tokens: List[str]) -> int:
        stack = []
        
        for token in tokens:
            if token.isnumeric() or token[1:].isnumeric():
                stack.append(int(token))
            elif token == "+":
                val = stack.pop() + stack.pop()
                stack.append(val)
            elif token == "-":
                val = -(stack.pop() - stack.pop())
                stack.append(val)
            elif token == "/":
                val2 = stack.pop()
                val1 = stack.pop()
                stack.append(int(val1 / val2))
            elif token == "*":
                val = stack.pop() * stack.pop()
                stack.append(val)
        
        return stack[-1]
```

- we can evaluate from the left by using a [[stack]].
- when we see an operator, we pop off the two most recent values in the stack, evaluate, and then push that new value onto the stack.
- note that we can do integer division truncating towards zero by doing `int(a / b)`.

Categories:: [[array]], [[math]], [[stack]]
