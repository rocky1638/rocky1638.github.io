---
created_at: 2022-11-12
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/flood-fill/
---

# 733. Flood Fill

An image is represented by an `m x n` integer grid `image` where `image[i][j]` represents the pixel value of the image.

You are also given three integers `sr`, `sc`, and `color`. You should perform a **flood fill** on the image starting from the pixel `image[sr][sc]`.

To perform a **flood fill**, consider the starting pixel, plus any pixels connected **4-directionally** to the starting pixel of the same color as the starting pixel, plus any pixels connected **4-directionally** to those pixels (also with the same color), and so on. Replace the color of all of the aforementioned pixels with `color`.

Return _the modified image after performing the flood fill_.

![](https://assets.leetcode.com/uploads/2021/06/01/flood1-grid.jpg)

```python
class Solution:
    def floodFill(self, image: List[List[int]], sr: int, sc: int, color: int) -> List[List[int]]:
        dirs = [[0,1],[1,0],[0,-1],[-1,0]]
        def dfs(i, j, starting_color):
            if i >= 0  and i < len(image) and j >= 0 and j < len(image[0]) and image[i][j] == starting_color and image[i][j] != color:
                image[i][j] = color
                for d in dirs:
                    dfs(i+d[0], j+d[1], starting_color)
        
        starting_color = image[sr][sc]
        dfs(sr, sc, starting_color)
        return image
```

- just a simple [[dfs]] and change the value of the neighboring nodes.

Categories:: [[dfs]], [[matrix]]
