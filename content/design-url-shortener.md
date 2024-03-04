---
title: "design url shortener"
type: system-design-example
aliases: []
date: 2022-12-08
updated: 2024-02-29
---

## my solution

### clarifying questions

- Should the short URL expire?
	- Should live for 100 years.
- Can the user create custom URLs, or will they always be auto-generated?
- How many requests?
	- 100M per month.

### functional requirements

- A long url should always map to a *unique* short url, i.e. there should be no collisions.
- When a user enters a short URL, our site should redirect them to their original URL.
	- Our short URL should not be kept in the history stack of their browser.
- Short URLs should be persistent.
- Custom URLs.

### non-functional requirements

- Read-heavy system; presumably a short URL is made to be shared, and so we expect many more reads than writes to our servers.
- 100M write requests per month ~ 40 write requests per second.
	- Assuming a read heavy system, let’s say 100:1, we can assume 4000 reads per second.
- Durability; we shouldn’t lose any data.
- Low latency; the user should have as little delay as possible between accessing the short URL and being redirected to their original URL.
- Storage: 100M write requests per month, with each storage

### api requirements

- `generateShortURL(longURL) -> shortURL`
- `retrieveLongURL(shortURL) -> longURL`
	- This should be an HTTP GET request that returns a redirect!

### data modeling

- We don’t need relationships between the links, so we will use a non-relational key-value store type database like AWS DynamoDB.
- Each entry will be something like `shortURL, originalURL, ...metadata`.
	- Assuming that long URLs are stripped of unnecessary query params, let’s say that each entry is 200B, then we accumulate 100M * 12 * 100 objects = 120B objects.
	- At 200B each, we get a total storage of 24TB.

### high-level design

![[url-shortener-diagram.png]]
- Just a basic application set up, the things of note are:
	- A load balancer in front of horizontally scaling servers to serve both read and write requests.
	- A single-leader replicated group of key-value store NoSQL databases to handle high read load.
		- 40 writes/second should be achievable with a single leader node on something like Cassandra.
	- A cache with something like Redis to store high-traffic keys in memory for fast access and to reduce load on database instances.
		- An eviction policy like LRU to keep frequently accessed keys in memory.

### specifics

- How to generate the actual short URL?
	- Not sure! My two ideas are to either pick the next possible combination, or use some sort of hashing.
		- With picking the next combination, there could be issues with race conditions when multiple concurrent requests try to grab the “next" combination.
- How long should the short URL be? Depends on how many unique combinations we need.
	- There are 62 unique alphanumeric characters. Having 6 characters gives us 57 billion combinations, 7 characters gives us about 1.5 trillion.
		- So, we’d probably need to start with 7 characters.

## positive feedback

- single leader replication was a good idea.

## critique

### general

- I need to start from a simple baseline diagram and only adding things to specifically solve functional/non-functional requirements.

### requirements

- Didn’t talk about length of short URLs.
- Forgot to mention that we need high availability.

### design

- Didn’t mention partitioning strategies for the database (only replication).
- Didn’t talk about replicating/partitioning the caches.
- Didn’t talk about exactly how to generate the keys?

## references

- https://www.youtube.com/watch?v=fMZMm_0ZhK4
