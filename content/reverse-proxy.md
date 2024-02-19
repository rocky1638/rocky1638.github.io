# Reverse Proxy

- a public face for your backend servers.
- can be used even when you only have one server behind it, unlike [[load-balancer]].
- don’t have to reveal any information about the actual backend servers, IP addresses, etc.
- directly serve static content without hitting your servers.
- things like [[nginx]] can support both [[load-balancer]] and [[reverse-proxy]].
- disadvantages.
	- increases complexity.
	- single point of failure, increasing number of reverse proxies increases complexity.

## References.
- https://www.nginx.com/resources/glossary/reverse-proxy-vs-load-balancer/