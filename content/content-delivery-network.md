# Content Delivery Networks (CDNs)

- globally distributed network of proxy servers that serve static content.
	- some CDNs like Cloudfront do support dynamic content.
- advantages.
	- users receive content from a CDN that’s close to them.
	- your servers do not have to serve the requests that CDNs can already serve.

- push CDNs.
	- receive new content whenever data changes on the server.
	- content is uploaded only when it is new or changed.
	- server is responsible for manually pushing changes to CDNs.
	- good for sites whose data does not update frequently.
- pull CDNs.
	- grab new content from the server when a user requests it.
	- set a TTL (time-to-live) for cached data to expire *(and to be re-pulled).*
	- good for sites that have heavy traffic.

- advantages.
	- users can access servers that are closer to them for lower latency.
- disadvantages.
	- can be costly.
	- content could be stale if TTL has not expired the data yet.
	- require URLs to point to the CDN instead of the server.


```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.
- http://www.travelblogadvice.com/technical/the-differences-between-push-and-pull-cdns/