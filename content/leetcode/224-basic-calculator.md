# 224. Basic Calculator

```python
class Solution:
    def calculate(self, s: str) -> int:
        # helper function        
        def evalExpression(op, x, y):
            if op == "+":
                return x + y
            elif op == "-":
                return x - y
        
        def recurse(idx):
            tally = 0
            prev_op = "+"
            
            while idx < len(s):
                char = s[idx]
                
                if char == "(":
                    idx, subtally = recurse(idx+1)
                    tally = evalExpression(prev_op, tally, subtally)
            
                elif char == ")":
                    return idx+1, tally
                
                elif char.isnumeric():
                    num_str = char
                    idx += 1
                    while idx < len(s) and s[idx].isnumeric():
                        num_str += s[idx]
                        idx += 1
                    tally = evalExpression(prev_op, tally, int(num_str))
                elif char in ["+", "-"]:
                    prev_op = char
                    idx += 1
                else:
                    idx += 1
            return tally
                
        return recurse(0)
```

- we use [[recursion]] to assess nested brackets.
	- when we see an open bracket, we go one level deeper with recursion.
	- when we see a closing bracket, we return with the next `idx` of the string *(after the closing bracket)* and the value that is returned from the expression in the brackets.
- keep track of previous operator, defaulting to the plus sign, so whenever we ingest a number, we use that operator with the running tally.
	- so when we read our first number, we just add it to zero.

[[math]], [[string]]