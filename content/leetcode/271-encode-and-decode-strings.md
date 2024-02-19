---
created_at: 2023-01-03
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/encode-and-decode-strings/
---

# 271. Encode And Decode Strings

## Non-ascii delimiter.

```python
class Codec:
    def encode(self, strs: List[str]) -> str:
        """Encodes a list of strings to a single string.
        """
        return "\U0001f600".join(strs)
        

    def decode(self, s: str) -> List[str]:
        """Decodes a single string to a list of strings.
        """
        return s.split("\U0001f600") 
```

- i just used the smile emoji lol.

## Chunked transfer encoding.

![fig](https://leetcode.com/problems/encode-and-decode-strings/solutions/328340/Figures/271/encodin.png)
- for each string, compute its length, and append a four character number in front of it in the encoded string.
- fairly easy and straightforward to decode this.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[string]], [[array]]
