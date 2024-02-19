# caching

![](https://github.com/donnemartin/system-design-primer/raw/master/images/Q6z24La.png)

- refers to in-memory caches such as [[memcached]] or [[redis]].
- they act as a buffering layer between your application and your data storage.
	- help to balance out loads between reads and writes on your servers.
- cache is very fast!
	- redis can do hundreds of thousands of read operations per second.
- caching can happen on the client-side, in [[content-delivery-network]], server-side.
- two ways to cache data server-side.
	- caching queries.
		- we cache query results, so the next time the exact query is run, we can just grab it from the cache.
		- downside is that if any value in that query result changes, the entire query result has to be removed from the cache.
	- caching objects.
		- cache objects/classes just like in [[object-oriented-programming]], and easily evict stuff based on when the object gets updated.
		- some things that are normally cached:
			- user sessions.
			- fully rendered `html` files.
			- social network friend relationships.
- cache update policies.
	- cache-aside.
		- ![300](https://github.com/donnemartin/system-design-primer/raw/master/images/ONjORqk.png)
		- cache doesn’t talk directly to storage.
		- client checks cache first, and on a cache-miss, the client grabs from the database and save the value to the cache.
		- memcached is generally used like this.
		- disadvantages.
			- each cache miss results in three trips.
			- cache data can become stale if it’s updated in the database.
				- make sure to have TTL set.
	- write-through.
		- application writes and reads everything to cache.
		- cache is in charge of updating the database synchronously.
		- disadvantages.
			- when a new node is created, entries won’t be cached until the values are updated in the database.
	- write-behind/write-back.
		- ![300](https://github.com/donnemartin/system-design-primer/raw/master/images/rgSrvjG.png)
		- same as write-through, but the cache updates the db asynchronously using a queue (see [[asynchronism]]).
		- disadvantages.
			- could be data loss if the cache goes down before the database is updated.
	- refresh-ahead.
		- configure the cache to automatically refresh entries before they expire.
			- highly dependent on if we can accurately predict what values will be needed in the future.
	- disadvantages.
		- need to maintain consistency between database and caches.
		- need to add redis or memcached to your application.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## references

- https://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache
