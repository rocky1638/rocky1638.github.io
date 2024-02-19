# 1656. Design an Ordered Stream

```python
class OrderedStream:

    def __init__(self, n: int):
        self.data = [None for i in range(n)]
        self.next_id = 1

    def insert(self, idKey: int, value: str) -> List[str]:
        self.data[idKey-1] = value
        
        i = idKey-1
        ret = []
        if idKey == self.next_id:
            while i < len(self.data) and self.data[i]:
                ret.append(self.data[i])
                self.next_id += 1
                i += 1
        return ret
```

- preallocate space in a list for all the incoming inserts.
- keep track of the next `idKey` that needs to be outputted, only output if that key has just been inserted.

[[array]], [[lc-system-design]]