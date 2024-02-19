# 409. Longest Palindrome

```python
class Solution:
    def longestPalindrome(self, s: str) -> int:
        count = Counter(s)
        ans = 0
        
        for key in count:
            num_pairs = count[key] // 2
            ans += num_pairs * 2
            count[key] -= num_pairs * 2
        
        for key in count:
            if count[key] > 0:
                ans += 1
                break
        
        return ans
```

- use a [[frequency-map]], then every count of two of the same letter can be used as part of a palindrome.
- at the end if any letters are left, we can use exactly one of them to put in the middle of our longest palindrome.

[[string]], [[hashmap]], [[greedy]]