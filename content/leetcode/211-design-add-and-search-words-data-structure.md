---
created_at: 2022-12-10
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/design-add-and-search-words-data-structure/
---

# 211. Design Add and Search Words Data Structure

Design a data structure that supports adding new words and finding if a string matches any previously added string.

Implement the `WordDictionary` class:

- `WordDictionary()` Initializes the object.
- `void addWord(word)` Adds `word` to the data structure, it can be matched later.
- `bool search(word)` Returns `true` if there is any string in the data structure that matches `word` or `false` otherwise. `word` may contain dots `'.'` where dots can be matched with any letter.

```python
class TrieNode:
    def __init__(self, val, end = False) -> None:
        self.val = val
        self.children = {}
        self.end = end

class WordDictionary:
    def __init__(self):
        self.root = TrieNode(None)

    def addWord(self, word: str) -> None:
        curnode = self.root
        for i, char in enumerate(word):
            if char in curnode.children:
                if i == len(word)-1: # this is the last character
                    curnode.children[char].end = True
                curnode = curnode.children[char]
            else:
                newnode = TrieNode(char)
                curnode.children[char] = newnode
                if i == len(word)-1: # this is the last character
                    newnode.end = True
                else:
                    curnode = newnode
                        
    def searchHelper(self, word, curnode) -> bool:
        for i, char in enumerate(word):
            # wild card recursive case
            if char == ".":
                if i == len(word)-1:
                    for child in curnode.children:
                        if curnode.children[child].end:
                            return True
                    return False

                for child in curnode.children:
                    found = self.searchHelper(word[i+1:], curnode.children[child])
                    if found: return True
                return False
            # if we find the char, keep searching
            if char in curnode.children:
                # if at the end, check if this node is an end node
                if i == len(word)-1:
                    if curnode.children[char].end:
                        return True
                    return False

                # advance search pointer
                curnode = curnode.children[char]
            else:
                return False
        

    def search(self, word: str) -> bool:
        return self.searchHelper(word, self.root) 


# Your WordDictionary object will be instantiated and called as such:
# obj = WordDictionary()
# obj.addWord(word)
# param_2 = obj.search(word)
```

- have to use a [[trie]] to store the words in our data structure.
- we use [[recursion]] with [[dfs]] to check when we see a wildcard character.

Categories:: [[lc-system-design]], [[string]], [[recursion]], [[trie]], [[dfs]]
