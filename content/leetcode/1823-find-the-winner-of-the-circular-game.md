# 1823. Find the Winner of the Circular Game

## Using array.

```python
class Solution:
    def findTheWinner(self, n: int, k: int) -> int:
        players = [None] + [1]*n
        still_in = set([i+1 for i in range(n)])
        
        cur = 0
        for _ in range(n-1):
            moves_left = k
            while moves_left > 0:
                # advance to next player
                cur = 1 if cur == n else cur + 1
                
                if players[cur] == 1: # player still in
                    moves_left -= 1
                else: # player already eliminated
                    continue
            # cur is now on the next player to be eliminated
            players[cur] = 0
            still_in.remove(cur)
        return list(still_in)[0]
```

- just simulate it with a big [[array]] and a set to remember who’s still in the game.

## Using queue.

```python
class Solution:
    def findTheWinner(self, n: int, k: int) -> int:
        friends = deque(range(1, n+1))
        
        while len(friends) > 1:
            # for the number of moves
            for _ in range(k-1):
                # friend who is popped is safe for now
                # he goes to the back of the line
                # this operates in the same way as a circle
                friends.append(friends.popleft())
            friends.popleft()
        return friends[0]
```

- we can think of a circle in which this game is played just as a line where anyone who’s turn it passes moves to the back of the line.
- this way, we can just move `k` people to the back of the line, and then eliminate the person at the front of the line.
- we do this using a [[queue]].