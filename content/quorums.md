---
created_at: 2022-12-29
type: concept
aliases: [quorum]
---

# Quorums

- in a multi-node system with $V$ nodes, we fix a number of nodes that have to agree on each read, $V_r$, and a number of nodes that must be written to for each write, $V_w$.
- a mechanism to achieve a balance between read and write speeds in [[database-replication]].

> [!example] an example.
> consider a system with three nodes, $V=3$.
>
> if we set $V_r = V_w = 2$, then every written value is saved to two replicas, and every read considers the values of two replicas.
>
> we are guaranteed for one replica to be a common element between these two sets of nodes, so are guaranteed to return the latest correct value to the client.

- our quorums should satisfy the following requirements:
	- $V_r + V_w > V$
		- this ensures that a read and write does not happen on the same data item concurrently.
		- if one of $V_r$ or $V_w$ is taken, then the other operation will not be able to find enough vacant nodes to perform their request.
	- $V_w > V/2$
		- this ensures that a data item will not be written to by two concurrent operations, and that there is always overlap on at least one node from subsequent operations.
- if we satisfy all of these requirements, than the [[distributed-systems|distributed system]] will behave as if it is a single non-replicated instance in the eyes of the client.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[network-asynchrony]]
- [[consistency-patterns]]

## References.

Categories:: [[distributed-systems]]
