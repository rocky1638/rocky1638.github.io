---
title: "design content delivery network"
tags:
aliases: 
parents: 
children: 
supports: 
enemies:
date: 2022-12-30
updated: 2024-03-02
---

## my solution

### what is it?

See [[content-delivery-network]].


### functional requirements

- Should serve HTTP requests from users.
- Should cache static content like HTML, images, videos.
	- Cached content should have an expiry date.
	- Cached content should be able to be updated when new data is available from the main database.

### non-functional requirements

- Low latency.
- High availability.
- Read heavy usage on the edge of the CDN network.

### high-level design

![[design-content-delivery-network-diagram.png]]

The orchestrator is now a SPOF! Perhaps we can potentially partition it so that orchestrators can be horizontally scaled, each handling CDN nodes with an ID in a certain range.

### specifics

- How do we notify the edge nodes that we have updated content?
	- Push CDNs are very high maintenance, so I think especially with a lot of CDN nodes, to just use a pull methodology.
		- On a cache miss, or when the item in the cache is past its TTL, pull latest from server.
- Force invalidate cache.
	- Central server can push request to invalidate specific key or group of key on CDNs.
		- On next request, fetch from server.
- How to handle CDN node outages?
	- DNS service should be aware of which nodes are alive with a one-way heartbeat from each CDN node.
	- When a CDN node hasn’t responded for $x$ expected heartbeats, mark it as down and redirect traffic.
		- Once the heartbeats come back online, re-enable traffic flow to it.

## positive feedback

- The basic idea behind caching multiple distributed nodes, geographically spaced, was correct.
- The initial call from the user through a DNS was correct.
- Pulling data/caching data/invalidating data was well handled and discussed.

## critique

### general

- Didn’t know that CDNs are also commonly used as a **reverse proxy**, or a man-in-the-middle.[^1]
	- They will directly serve static content, and then forward requests for dynamic content to the internal sphere of the server (load balancer, server, database, etc.)
	- This is safer as only your CDNs are ever exposed to public networks.

### ingress

- Didn’t talk about Anycast protocol.
	- With Anycast, multiple nodes can share the same IP address, with the closest server receiving the traffic.
- Added in an unnecessary “orchestrator” node, when in reality the distributed DNS server is the one that routes traffic to geographically close CDN nodes, as well as handling backup routing in the case of outages. (In the unicast approach, as opposed to Anycast).

## references

- https://www.youtube.com/watch?v=8zX0rue2Hic
- https://developers.cloudflare.com/reference-architecture/architectures/cdn/#routing-requests-to-cdn-nodes

[^1]: https://www.reddit.com/r/sre/comments/soonzu/comment/hwaq2st/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button
