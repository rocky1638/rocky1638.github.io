---
title: "eventual consistency"
created_at: 2022-12-31
type: concept
aliases: []
---

A simplified consistency heuristic that states that all nodes in a system are guaranteed to reach a consistent state after an infinite amount of time.

> [!warning] An oversimplification?
> Unfortunately, eventual consistency is not very useful in practice, as a system that becomes consistent after a long period of time (say, hours or days) is not useful for real-life applications.

In general, data or state that is updated asynchronously will have an eventual consistency guarantee. *(See [[database-replication#asynchronous vs. synchronous replication]].)*
