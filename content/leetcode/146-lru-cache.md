---
created_at: 2022-11-23
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/lru-cache/
---

# 146. LRU Cache

```python
"""
We create a doubly-linked list with a hashmap
Hashmap points to the reference for the node in the DLL
"""

class Node:
    def __init__(self, val, key, left = None, right = None):
        self.val = val
        self.left = left
        self.right = right
        self.key = key

class LRUCache:
    def __init__(self, capacity: int):
        # doubly linked list (goes head->tail left->right)
        # most recent is at the HEAD
        # initialized as HEAD <-> TAIL
        self.head = Node(-1, -1)
        self.tail = Node(-1, -1)
        self.head.right = self.tail
        self.tail.left = self.head
        self.cache_size = 0
        self.capacity = capacity
        
        # hashmap { key: Node }
        self.d = {}
        
    def _printList(self):
        out = []
        cur = self.head.right
        while cur != self.tail:
            out.append(cur.val)
            cur = cur.right
        print(out)
        
    def insertIntoList(self, key):
        keynode = self.d[key]
        right_of_head = self.head.right
        
        self.head.right = keynode
        keynode.left = self.head
        keynode.right = right_of_head
        right_of_head.left = keynode
        
    def makeMostRecent(self, key):
        keynode = self.d[key]
        lok = keynode.left
        rok = keynode.right
        
        # connect lok and rok together
        lok.right = rok
        rok.left = lok
        
        # insert keynode between head and roh
        roh = self.head.right
        
        self.head.right = keynode
        keynode.left = self.head
        keynode.right = roh
        roh.left = keynode
        
    def evictLeastRecentlyUsed(self):
        lru_node = self.tail.left
        left_of_lru = lru_node.left
        
        left_of_lru.right = self.tail
        self.tail.left = left_of_lru
        
        self.cache_size -= 1
        del self.d[lru_node.key]

    def get(self, key: int) -> int:
        # check in dict to see if key exists
        if key in self.d:
            # move accessed key node to HEAD <-> NODE(key) <-> .... TAIL
            self.makeMostRecent(key)
            # return node value
            return self.d[key].val
        else:
            return -1

    def put(self, key: int, value: int) -> None:
        if key in self.d:
        # if key already in here, update value and move to most recently used
            keynode = self.d[key]
            keynode.val = value
            self.makeMostRecent(key)
        else:
        # else, create node and also move to most recently used
            newnode = Node(value, key)
            self.d[key] = newnode
            self.insertIntoList(key)
            self.cache_size += 1
            # check cache size and if it's over, evict least recently used (TAIL.left)
            if self.cache_size > self.capacity:
                self.evictLeastRecentlyUsed()
```

- we use a [[linked-list]], more specifically, a [[doubly-linked-list]] to keep the nodes in the order of most recently used.
- we use a [[hashmap]] to map the `key` values to the nodes in the list.
- just be careful with updating pointers when accessing or inserting items.

Categories:: [[linked-list]], [[doubly-linked-list]], [[hashmap]]
