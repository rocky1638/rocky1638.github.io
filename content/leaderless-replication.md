---
title: "leaderless replication"
created_at: 2024-01-28
type: concept
aliases: 
parents:
  - "[[database-replication]]"
children: 
supports: 
enemies:
---

Leaderless replication is characterized by each node in the system being allowed to take reads and writes.

![[quorum-read-and-write-diagram.png|Figure 1: Reads and writes in leaderless scheme.]]

## how to propagate writes to all nodes?

Just like with [[multi-leader-replication]], only asynchronous replication makes sense, as using synchronous replication would negate the throughput and availability benefits of leaderless replication.

There are two ways we can propagate writes.

### read repair

On each read request, the client receives responses from multiple nodes. The client will use the value from the most recent write, but can send write requests to the replicas that returned stale values.

This works best in a system where values are read frequently. However, values can get very out-of-date if they are not read very often.

### anti-entropy

A background process runs in your database system, finding mismatched values and updating them. _(Kind of like a garbage collector)._

## quorum reads and writes

**Quorum reads and writes** let us guarantee that we receive the latest value from the database without waiting for all nodes. This increases **availability**.

The basic rule is that for a system with $n$ nodes,

$$
\begin{align}
r+w \gt n
\end{align}
$$

where $r$ and $w$ are the number of responses we require for reads and writes, respectively.

![[quorum-diagram.png|Figure 2: Quorum read and write.]]

Although this is mathematically solid, there are still some issues that can arise due to asynchronicity. For example:

- If a write and a read happen concurrently, the new write may not have been written to all $w$ replicas yet, meaning that the read grabs a set of $r$ replicas that haven’t received the new write yet.
- If a node carrying a new value fails and is restored by a node with old value, there could be less than $w$ nodes carrying the new value, breaking the quorum.

### sloppy quorum

- in even bigger systems, each value could have a set of $n$ nodes in which its stored, even if there are more than $n$ total replicas.
	- in downtime, the home nodes may be unaccessable while other nodes still are.
	- these nodes can pick up the slack and then share the data back to home nodes after they’re back up.
	- just more write availability and durability, but doesn’t give quorum consistency
