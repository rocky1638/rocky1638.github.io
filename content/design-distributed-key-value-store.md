---
title: "design distributed key-value store"
tags:
aliases: 
parents: 
children: 
supports: 
enemies:
date: 2022-12-30
updated: 2024-03-09
---

## my solution

### functional requirements

- A user can retrieve the value for a key, if they have read credentials.
- User can save or update the value of a key that they have the write credentials for.

### non-functional requirements

- Value retrieval with a key should be low latency.
- Consistency guarantees.
	- Depends on the use case, for sensitive/high-stakes use cases, we’d probably want to guarantee some sort of strong consistency using 2PC (two phase commit).
	- For cases where many users are writing keys to the key-value store and most users only care about a few keys, simple causal consistency guarantees like read-your-writes would probably be sufficient.
- We can likely assume that we’ll have many more reads than writes, as the typical use-case for key-value stores is to store values and reference them later with low latency/without recomputing.
	- Can confirm with interviewer if this is an acceptable assumption, because there are definitely times when this isn’t the case.

### api design

- `create_or_update(key, value)`
- `get_value(key)`

### design specifics

![[design-distributed-key-value-store-diagram.png]]

- Questions we need to answer:
	- How do we avoid conflicting keys from concurrent writes?
		- Using a single-leader model for each partition, we can use a simple LWW (last-write-wins) heuristic to fail any concurrent request that uses the same key as a previous request.
			- Because there is a single-leader, we can maintain total global ordering of requests without sacrificing latency with something like two-phase commit if we had multiple leaders.
	- How do we construct keys? Do we just use the ones that the user provides?[^1]
		- I think this is fine? We can partition the keys by alphabetical grouping.
- Partitioning details:
	- If keys are not distributed evenly by alphabetical order, we could consider hashing to evenly space the values (we could also consider consistent hashing if we need to frequently change the number of active partitions).

## positive feedback

## critique

## references

- https://www.youtube.com/watch?v=rnZmdmlR-2M

[^1]: I would ask the interviewer what the expected use case for this application/key-value store is. If it is for a single system to use, we could continue with allowing the application to figure out how keep their own keys from conflicting. However, it’s for users anywhere to store a value in a global key-value store, we could use some unique user identifier appended to the user’s key. We could then partition by user locations or IP addresses.
