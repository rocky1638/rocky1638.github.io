# 380. Insert Delete GetRandom O(1)

## Naive approach.

```python
class RandomizedSet:

    def __init__(self):
        self.set = set()

    def insert(self, val: int) -> bool:
        if val in self.set:
            return False
        
        self.set.add(val)
        return True
        

    def remove(self, val: int) -> bool:
        if val in self.set:
            self.set.remove(val)
            return True
        
        return False

	# this doesn't work because it's O(n)!
    def getRandom(self) -> int:
        return random.choice(list(self.set))
```

- `insert` and `remove` are $O(1)$, but `getRandom` is not.

## Better approach.

```python
class RandomizedSet:

    def __init__(self):
        # { val: index_of_val_in_data }
        self.map = {}
        self.data = []

    def insert(self, val: int) -> bool:
        if val in self.map:
            return False
        
        self.data.append(val)
        self.map[val] = len(self.data)-1
        return True
        

    def remove(self, val: int) -> bool:
        if val in self.map:
            if len(self.data) == 1:
                self.data = []
                self.map.clear()
                return True
            
            idx_of_val = self.map[val]
            last_element = self.data[-1]
            
            # update idx of last_element in map
            self.map[last_element] = idx_of_val
            
            # swap val and last_element
            self.data[-1], self.data[idx_of_val] = self.data[idx_of_val], self.data[-1]
            
            # remove val from map
            self.map.pop(val)
            # remove val from data
            self.data.pop()
            
            return True
        
        return False
```

- we manually keep track of our values in a pseudo-set by combining a [[hashmap]] and an [[array]].
- this way, we don’t have to convert our set to an array everytime `getRandom` is called.

[[lc-system-design]]