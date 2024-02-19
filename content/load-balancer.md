# Load Balancers

- distribute incoming client requests to servers/databases.
	- prevent requests from going to unhealthy servers.
	- eliminate single points of failure.
- load balancers can do fancy request encryption so the servers don’t have to.
- can maintain session persistence by routing users to the correct servers.
- common to set up multiple load balancers using active-active or active-passive.
	- similar methodology to [[database-replication]].
- ways to route traffic:
	- [[round-robin]].
	- [[layer-4]].
		- look at info in the transport layer including IP address, header ports, and packet contents.
	- [[layer-7]].
		- look at info in the application layer.
		- do more specific rerouting, like directly video traffic to video-hosting servers and user billing traffic to more secure servers.
		- [[layer-4]] balancing is typically less compute-heavy but is less flexible.
- disadvantages.
	- can become a bottleneck.
	- a single load balancer is a single point of failure.
