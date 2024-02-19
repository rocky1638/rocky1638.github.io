# 232. Implement Queue Using Stacks

```python
class MyQueue:

    def __init__(self):
        self.s1 = []
        self.s2 = []

    def push(self, x: int) -> None:
        self.s1.append(x)

    def pop(self) -> int:
        while len(self.s1):
            self.s2.append(self.s1.pop())
        
        val = self.s2.pop()
        
        while len(self.s2):
            self.s1.append(self.s2.pop())
            
        return val
        

    def peek(self) -> int:
        return self.s1[0]

    def empty(self) -> bool:
        return len(self.s1) == 0
```

- when popping, just pop everything to the other stack to get at the bottom element, and then pop everything back.
	- we can optimize by never having to push the values back into the first stack!

```python
class MyQueue:

    def __init__(self):
        self.s1 = []
        self.s2 = []

    def push(self, x: int) -> None:
        self.s1.append(x)

    def pop(self) -> int:
        if not len(self.s2):
            self.transfer()

        return self.s2.pop()
        

    def peek(self) -> int:
        if not len(self.s2):
            self.transfer()
        return self.s2[-1]

    def empty(self) -> bool:
        return len(self.s1) == 0 and len(self.s2) == 0
    
    def transfer(self) -> None:
        while len(self.s1):
            self.s2.append(self.s1.pop())
```

[[stack]], [[queue]], [[array]]