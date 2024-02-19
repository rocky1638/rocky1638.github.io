# Rate Limiter Design

- how do we identify users?
	- unique identifier such as ip address or user ids.
- what logic do we actually use to rate limit?
	- tokens in a bucket.
		- have tokens regenerate for each user per time unit *(up to a maximum number of tokens)*.
		- each time a request comes in, use a token if it’s available.
			- drop the request if there’s no tokens available currently.
	- maximum number of requests in a time window.
		- can be bad if a lot of requests come at the beginning of the window, because no requests will be allowed for the rest of the window.
- components.
	- rule engine to specify tunable parameters.
	- high throughput cache to store all the data of each user’s requests.
	- logging service.
		- nosql database.

![[rate-limiter.excalidraw|100%]]
