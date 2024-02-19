# system design interview: an insider’s guide by alex yu

## chapter 1. how to scale a website to millions of users

- The most simple system design is a user accessing a webpage.
	- Users access websites through domain names, which are linked to actual IP addresses.
	- The **user must call a Domain Name System, or DNS** to get the actual IP address.
	- After that, an HTTP request is made to the server, which sends back some response.

### request handling scaling

- **Vertical scaling** is the process of **adding more power to scale**.
	- It is simple, but **has a hard limit** and gets exponentially more **expensive**.
	- **Lacks redundancy**, has single point of failure.
- **Horizontal scaling** is the process of adding more machines to scale.
	- We can use **load balancers** to evenly distribute incoming requests between our servers.
		- Users connect to the load balancer directly, which then redirects the request to the appropriate server *(the actual servers are private IP addresses)*.
		- When one server goes down or requests increase, we can reroute requests and add servers as needed.

#### stateful vs. stateless architecture

- We can design our web apps with either stateless or stateful architecture.
	- Stateful architecture, relies on **storing user profile data and session data on a server**.
		- The main downside with this is that all requests by a single user must go through the same server, which makes it **hard to horizontally scale**.
	- Stateless architectures **store session data in a shared database**, so that any user can make any request to any server at any time.
		- Because session data is typically not inter-related, **NoSQL databases are typically used for this** use case.

#### data centers

- We can further scale horizontally by having multiple data centers, with a load balancer that redirects requests to the **geographically closest data center**.
	- Data centers contain servers, caches, and databases.
	- Some considerations:
		- GeoDNS can be used to direct traffic to the nearest data center.
		- We have to somehow synchronize data between data centers. An easy way to do this is to **replicate data across multiple data centers**.

#### message queues

- To further scale, we need to decouple common aspects of our app so they can scale independently.
- A message queue is a component that is **stored in memory to support asynchronous communication**.
	- We have **producers that publish jobs to the queue, and then consumers that subscribe to the queue and process those jobs**.
		- This allows a decoupling between producers and consumers because producers can enqueue jobs, even when consumers are unavailable.
		- The number of producers and consumers can be **scaled independently**.

### database scaling

- When we want to scale our data collection and usage, we need to have a database which will require separate web traffic.

#### when to use relational vs. non-relational databases?

- **Relational DBs support joins** where as non-relational DBs do not.
- We might elect to use a non-relational DB when:
	- We require **super low latency**.
	- Our **data is unstructured** and unrelated to each other.
		- We need to store **massive amounts of data**.

#### master and slave databases

We can horizontally scale databases by using [[single-leader-replication]].

#### sharding

- Just like with servers, we can scale databases either horizontally or vertically.
	- Scaling vertically has the same problems as scaling servers vertically *(expensive, single point of failure)*.
	- We scale databases vertically using a technique called **sharding**.
		- We separate a large database into smaller, more manageable sections, called shards.
		- Then, we **determine which shard to save data on using a hash function** without collisions.
			- We need to make sure that the sharding key, or the values that are hashed, will actually lead to a **well distributed set of data**.
		- Common issues:
			- The celebrity problem, also known as a hotspot key problem is when certain shard keys receive an abnormally large amount of requests.
			- Joins get much harder once all of our data is split up and sharded.
				- A common workaround is to denormalize the database.

#### caching

- We can put a cache between a database and a server to store frequently accessed data, so we don’t have to do expensive database queries all the time.
	- Server **first checks the cache, and then goes to the database only when necessary**.
- Important considerations when using a cache include:
	- Use a cache when data is read frequently and modified infrequently. Caches should not be used for persisting data.
	- **Implement a way for data to expire**. Has to be a balance, because we don’t want data to become stale but we also don't want to be called on the database too often.
	- We have to make sure that the data in the cache, and the actual database remains in sync. Ensure that the cache values are cleared or updated when the underlying value in the database is updated.
	- Consider using **eviction policies** such as LRU (least recently used), LFU (least frequently used), or FIFO (first in first out).

##### cdn’s are caches for static data

- CDN’s or content delivery networks are a **special spread-out network of caches for static content**.
	- The link that the user accesses is actually the link to the CDN server, and not the main server.
		- If it’s in the CDN, it’s returned. Else, the CDN requests the file from the server and caches it.
	- Considerations include:
		- Costs, because CDNs are often run by third parties.
		- Just like with normal caches, TTL (time-to-live) is important to tune properly.
		- You should have a way to invalidate the files in your CDN.

## chapter 2. back-of-envelope calculations

- General rules of thumb:
	- Memory is fast but disk reads are slow.
	- Compress data before sending it over the internet.
- We can estimate the queries-per-second (QPS) by using daily active users/activity of the average user.
- Tips for estimation questions:
	- Approximate numbers.
	- Write down your assumptions.
	- Commonly asked values include QPS, peak QPS, storage, cache, and number of servers.

## chapter 3. how to approach system design interviews

- The final design is less important compared to the work you put in the design process.
- It’s more about the collaborative process of problem-solving with your interviewer.

### 4-step process for system design interviews

- Step 1: Understand the problem and establish design scope: 3-10 minutes
- Step 2: Propose high-level design and get buy-in: 10-15 minutes
- Step 3: Design deep dive: 10-25 minutes
- Step 4: Wrap: 3-5 minutes

 1. **Understand the problem and establish scope.**

- Ask basic requirement questions and write down assumptions.
	- What are the most important features for the product? *(This is likely what you’ll actually be designing).*
	- How many users does the product have? Daily traffic?
	- What is the company’s technology stack? What existing services you might leverage to simplify the design?

2. **Propose high-level design and get buy-in.**

- Treat your interviewer as a teammate!
- Draw box diagrams.
	- Clients, APIs, servers, data stores, caches, CDN, message queues, etc.
- Do estimates to make sure the scale fits, ask interviewer if this is even necessary.

> "Should we include API endpoints and database schema here? This depends on the problem. For large design problems like “Design Google search engine”, this is a bit of too low level. For a problem like designing the backend for a multi-player poker game, this is a fair game. Communicate with your interviewer.”

3. **Deep dive.**

- Dive deep into a few of the interesting problems with the design. Work with the interviewer to figure out what you should focus on.

4. **Wrap up, next steps.**

- Identify bottlenecks, discuss possible improvements.
- Give a recap.
- Error cases can be interesting to talk about.
- How do we scale the current design to the next scale?

## chapter 4. rate limiting

- Rate limiting can be done at any point in the stack.
	- Doing it as middleware or in the server can give us more control, a little more safe from malicious entities on the client side.
- Cache rules are typically stored on disk somewhere, and can be cached.
- Rate limited requests can either be dropped or put into a queue somewhere to eventually be fulfilled.
- Send feedback to client if a request was rate-limited.
- Various algorithms can be used for rate limiting including:
	- Token bucket
	- Leaking bucket
	- Fixed window
	- Sliding window log
	- Sliding window counter
- Typically want to store counter values in a fast cache such as Redis.
	- Centralizing this data also allows us to horizontally scale our actual rate limiter devices, so they can share data in a stateless system.
