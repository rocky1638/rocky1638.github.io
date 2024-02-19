# 723. Candy Crush

```python
class Solution(object):
    def candyCrush(self, board):
        R, C = len(board), len(board[0])
        todo = False

		### CRUSHING ###

        for r in range(R): # for each row
            for c in range(C-2): # sliding window of length 3
                # if all items in window are same, mark for deletion
                if abs(board[r][c]) == abs(board[r][c+1]) == abs(board[r][c+2]) != 0:
                    board[r][c] = board[r][c+1] = board[r][c+2] = -abs(board[r][c])
                    todo = True

        for r in range(R-2): # sliding window of height 3
            for c in range(C): # for each column
                # if all items in window are same, mark for deletion
                if abs(board[r][c]) == abs(board[r+1][c]) == abs(board[r+2][c]) != 0:
                    board[r][c] = board[r+1][c] = board[r+2][c] = -abs(board[r][c])
                    todo = True

		### GRAVITY ###
		
        for c in range(C): # for each column
            wr = R-1 # set write head to be at bottom of column
            for r in range(R-1, -1, -1): # r is read head, starts at write head and moves up
                if board[r][c] > 0: # if value at read head is not 0, write it to write head
                    board[wr][c] = board[r][c]
                    wr -= 1 # move write head up
            for wr in range(wr, -1, -1): # fill remaining column with 0s
                board[wr][c] = 0

        return self.candyCrush(board) if todo else board
```

- very implementation heavy question.
- we repeatedly conduct “crushing” and “gravity” steps until the board is stable.
- most efficient way and conceptual way to do this is by using a [[sliding-window]] approach for both steps.
	- for the crushing step, whenever three values in the window are the same, mark them all for deletion.
		- we need to lazy delete, because a number could be part of a connected sequence both horizontally and vertically.
	- for the gravity step, use a variable size sliding window with a read and write pointer.
		- start at the bottom of the column, and “shift” all the non-zero values to the bottom, and fill the remaining column with zeroes up to the top.

[[array]], [[matrix]], [[sliding-window]]