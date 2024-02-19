---
type: course
---

# system design primer

- performance vs. scalability.
	- performance is when the system is fast for a single user.
	- scalability is when the service is fast for many users.
- latency vs. throughput.
	- latency is the time it takes to perform an action or produce a result.
	- throughput is the number of these actions per unit of time.
- [[cap-theorem]].
	- [[consistency-patterns]].
	- [[availability]]
	- [[availability-patterns]].
- [[content-delivery-network]].
- [[load-balancer]].
- [[reverse-proxy]].
- [[microservices]] in the application layer.
	- services such as consul, etcd, and zookeeper can help your microservices talk to each other.
	- disadvantages.
		- microservices add complexity.
- ways to scale [[database|databases]].
	- [[database-replication]].
	- [[database-federation]].
	- [[database-sharding]].
	- [[denormalization]].
- [[nosql-database]].
- sql vs [[nosql-database]].
	- sql advantages.
		- structured data/strict schemas.
		- complex joins/relational data.
		- transactions.
	- [[nosql-database]] advantages.
		- dynamic schema.
		- non-relational data.
		- if you don’t need complex joins.
		- can store lots of data.
		- examples:
			- log data.
			- leaderboard data.
			- temporary data.
			- metadata.
- [[caching]]
- [[asynchronism]].
- [[methods-of-communication]].

## references

- https://github.com/donnemartin/system-design-primer

## further reading

- https://lethain.com/introduction-to-architecting-systems-for-scale/
