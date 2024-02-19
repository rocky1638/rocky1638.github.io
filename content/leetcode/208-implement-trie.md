---
created_at: 2022-11-20
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/implement-trie-prefix-tree/
---

# 208. Implement Trie

```python
class TrieNode:
    def __init__(self, char, end):
        self.char = char
        self.end = end
        self.children = {} # { char: TrieNode, ... }

class Trie:
    def __init__(self):
        # dict of TrieNodes { char: TrieNode, char: TrieNode, ... }
        self.root = TrieNode(None, True)

    def insert(self, word: str) -> None:
        curnode = self.root
        for i, char in enumerate(word):
            if char not in curnode.children:
                new_node = TrieNode(char, i == len(word)-1)
                curnode.children[char] = new_node
            curnode = curnode.children[char]
        curnode.end = True

    def search(self, word: str) -> bool:
        curnode = self.root
        for char in word:
            if char in curnode.children:
                curnode = curnode.children[char]
            else:
                return False
        return curnode.end
        
    def startsWith(self, prefix: str) -> bool:
        curnode = self.root
        for char in prefix:
            if char in curnode.children:
                curnode = curnode.children[char]
            else:
                return False
        return True
```

- standard implementation of a [[trie]].

Categories:: [[trie]]
