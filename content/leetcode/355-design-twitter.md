---
created_at: 2023-01-12
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/design-twitter/
---

# 355. Design Twitter

Design a simplified version of Twitter where users can post tweets, follow/unfollow another user, and is able to see the `10` most recent tweets in the user's news feed.

Implement the `Twitter` class:

- `Twitter()` Initializes your twitter object.
- `void postTweet(int userId, int tweetId)` Composes a new tweet with ID `tweetId` by the user `userId`. Each call to this function will be made with a unique `tweetId`.
- `List<Integer> getNewsFeed(int userId)` Retrieves the `10` most recent tweet IDs in the user's news feed. Each item in the news feed must be posted by users who the user followed or by the user themself. Tweets must be **ordered from most recent to least recent**.
- `void follow(int followerId, int followeeId)` The user with ID `followerId` started following the user with ID `followeeId`.
- `void unfollow(int followerId, int followeeId)` The user with ID `followerId` started unfollowing the user with ID `followeeId`.

```python
class Twitter:

    def __init__(self):
        # graph[user] = [list of ppl user is following]
        self.graph = collections.defaultdict(set)
        self.posts = collections.defaultdict(list)
        self.counter = -1

    def postTweet(self, userId: int, tweetId: int) -> None:
        # the smaller the number, the newer the tweet is
        self.posts[userId].append((self.counter, tweetId))
        self.counter -= 1
        
    def getNewsFeed(self, userId: int) -> List[int]:
        feed = []

        # user "follows" themselves
        self.graph[userId].add(userId)

        # accumulate all posts
        for following in list(self.graph[userId]):
            for i, post in enumerate(self.posts[following]):
                heapq.heappush(feed, post)
 
        ret = []
        for _ in range(10):
            if len(feed):
                ret.append(heapq.heappop(feed)[1])
        return ret


    def follow(self, followerId: int, followeeId: int) -> None:
        self.graph[followerId].add(followeeId)

    def unfollow(self, followerId: int, followeeId: int) -> None:
        if followeeId in self.graph[followerId]:
            self.graph[followerId].remove(followeeId)
```

- we store all user relationships in a adjacency list graph.
- we store all posts in a hashmap.
- we use a running counter to keep track of which tweets were posted first.
- on call to `getNewsFeed`, we heap all of the $k$ most recent posts from each user the calling user is following, and grab the top $k$ from the heap.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[heap]], [[priority-queue]], [[hashmap]], [[array]], [[lc-system-design]]
