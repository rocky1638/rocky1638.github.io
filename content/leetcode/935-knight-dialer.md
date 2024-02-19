# 935. Knight Dialer

```python
class Solution:
    def knightDialer(self, n: int) -> int:
        moves = {
            1: [6, 8],
            2: [7, 9],
            3: [4, 8],
            4: [0, 3, 9],
            5: [],
            6: [0, 1, 7],
            7: [2, 6],
            8: [1, 3],
            9: [2, 4],
            0: [4, 6]
        }
        
        # keep track of number of numbers ending with each digit
        dp = {
            0: 1,
            1: 1,
            2: 1,
            3: 1,
            4: 1,
            5: 1,
            6: 1,
            7: 1,
            8: 1,
            9: 1
        }
        
        for i in range(1, n):
            to_add = [0]*10
            for key in dp:
                for next_num in moves[key]:
                    to_add[next_num] += dp[key]
            for i in range(len(to_add)):
                dp[i] = to_add[i]
        
        return sum(dp.values()) % (10**9+7)
```

- i first tried to use [[backtracking]] and [[recursion]] to solve the problem but it timed out.
- we can solve this using bottom-up [[dynamic-programming]].
	- from each number, we know what the next numbers can be.
	- working bottom up, we keep track in our [[hashmap]] `dp` the number of possible phone numbers of length `i` that end with each digit.
	- then, given that $n$ phone numbers of length $i$ end with digit $x$, we know that all of these $n$ phone numbers can become phone numbers of length $i+1$ that end with `moves[x]`.
		- for example, we know that the number of phone numbers of length $i+1$ that end with digit 6 is equal to the sum of the number of phone numbers of length $i$ that end with 1, 7, and 0 *(because those are the only numbers with 6 in their `moves` array)*.