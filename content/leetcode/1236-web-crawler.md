# 1236. Web Crawler

```python
class Solution:
    def crawl(self, startUrl: str, htmlParser: 'HtmlParser') -> List[str]:
        visited = {startUrl}
        domain = startUrl.split("http://")[1].split("/")[0]
        ans = [startUrl]
        queue = deque([startUrl])
        
        while queue:
            url = queue.popleft()
            check = htmlParser.getUrls(url)
            for new_url in check:
                if new_url in visited:
                    continue
                if new_url.split("http://")[1].split("/")[0] != domain:
                    continue
                ans.append(new_url)
                visited.add(new_url)
                queue.append(new_url)        
        return ans
```

- simple [[bfs]] with some [[string]] manipulation required for checking if the hostnames are the same.