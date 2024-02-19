# CS75 Scalability Lecture

- vps (virtual private server) vs. shared web host.
	- vps gives you a personal slice of some hardware on a machine.
		- an example of a vps service is amazon ec2.
	- a shared web host might have you sharing the same hardware at the same time with other users.
- scaling vertically vs. horizontally.
	- vertical scaling means adding more ram, more computer power, etc.
		- is **limited by the state-of-the-art level of current compute power**, eventually there is no computer that’s strong enough.
		- is not sustainable if you want to scale indefinitely.
	- horizontal scaling.
		- don’t use state-of-the-art hardware, we **expand sideways**.
		- we use a whole bunch of servers.
		- **distribute requests** over the webservers that we do have.
	- [[load-balancer]].
		- examples include:
			- amazon elb (elastic load balancer)
		- load balancers can run in parallel with two load balancers.
			- they run in active-active or active-parallel mode.
				- if one goes down, the other one will take all requests.
			- similar to master-master with databases.
		- instead of dns returning the address of a server, we return the ip of the [[load-balancer]].
			- servers can have private ip addresses.
		- how to balance load?
			- we can use different heuristics to balance load, without even using a [[load-balancer]].
				- [[round-robin]].
					- we can just cycle through the available servers in order to balance requests per user.
					- don’t need bidirectional communication between [[load-balancer]] and servers.
					- downside: users could be putting different loads on a server, leading to imbalance.
					- downside: sessions are typically implemented per server, how do we use round robin with this?
				- **servers can be responsible for different types of data**, like html or images or videos.
	- how to handle sessions/user-data in a horizontally distributed system?
		- the same user, accessing at different times (within the same TTL) should hit the same backend server.
		- use cookies?
			- storing everything in cookies is bad for privacy.
			- maybe just store the server id in the cookie?
				- could work, but what happens if that server goes down?
				- what if the ip changes?
				- we shouldn’t share our private ip scheme.
		- we could introduce a database for our sessions?
			- however, now if that database goes down, our redundancy in our servers is irrelevant.
		- store a big random number, and have the load balancer remember how to map them to servers.
- [[caching]].
	- `.html` files directly being shown to a user is a simple version of caching.
		- the html files are created beforehand, and just served from disk.
	- mysql provides caching for identical queries that are run multiple times.
	- **[[memcached]] is a memory cache** that is run on a server.
		- a key value storage mechanism.
		- we can store users keyed by their ids.
	- caches can get too big to the point where they run out of storage.
		- we can **have eviction policies to expire objects**.
		- everytime we get a cache hit, we update the most recently used timestamp.
			- MRU, LRU, FIFO are various eviction policies.
- [[raid]]
	- how do we ensure shared storage is reliable and redundant?
		- RAID which stands for redundant array of independent disks allows us to back up data onto multiple drives redundantly.
			- can be used to make sure that if a drive fails, we still have the data.
			- decrease the probability of downtime, but doesn’t protect against everything such as access to power, ram, etc.
- [[database-replication]].
	- one master database, and many follower slave databases.
	- everytime a query is executed on master, it’s copied down to the slaves.
	- when master goes down, we can just promote a slave to master.
	- good for read-heavy use cases but not for write-heavy.
		- write heavy use-cases will require all the slave databases to be updated.
	 - we can instead have a master-master setup.
		 - load balance across both of the master databases.
- [[database-partitioning]].
	- how do we decide what data goes in what partition?
		- could simply just put users with first half of the alphabet in one partition, second half of alphabet in the second partition.

## References.

- https://www.youtube.com/watch?v=-W9F__D3oY4

Type:: #lecture
Categories:: [[scalability]], [[system-design]]
