---
created_at: 2022-12-21
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/longest-repeating-character-replacement/
---

# 424. Longest Repeating Character Replacement

You are given a string `s` and an integer `k`. You can choose any character of the string and change it to any other uppercase English character. You can perform this operation at most `k` times.

Return _the length of the longest substring containing the same letter you can get after performing the above operations_.

```python
class Solution:
    def characterReplacement(self, s: str, k: int) -> int:
        ans = 0

        l = 0
        base = s[l]
        freq = collections.Counter()

        for r in range(len(s)):
            # update counter for current char
            freq[s[r]] += 1

            # consider most common char in string as main
            cur_most_common = max(freq, key=freq.get)
            if freq[cur_most_common] > freq[base]:
                base = cur_most_common
            
            numdiff = sum(freq.values()) - freq[base]
            while numdiff > k:
                freq[s[l]] -= 1
                l += 1

                cur_most_common = max(freq, key=freq.get)
                if freq[cur_most_common] > freq[base]:
                    base = cur_most_common
                numdiff = sum(freq.values()) - freq[base]

            # update ans
            ans = max(ans, r-l+1)
        return ans
```

- we use a [[sliding-window]] approach.
- we keep track of the frequency of characters in our window with a [[frequency-map]] or [[hashmap]].
- at every character, we have to consider the _most common character_ as the main character.
	- if after choosing our main character, there are more than `k` other characters in the window, we slide the left pointer up until there are less than `k` other characters.
		- note that the “main" character may change during this process, so we have to update our “main” character after each removal from the left.

Categories:: [[string]], [[sliding-window]], [[hashmap]], [[frequency-map]]
