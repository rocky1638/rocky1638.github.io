---
created_at: 2022-12-31
type: concept
aliases: [linearizability]
---

# Strong Consistency

![[strong-consistency-diagram.png]]
- subsequent reads will see the new data after a write.
- data is propagated with [[synchronous-replication]].
- seen in file systems and [[database|databases]], with [[database-transaction|transactions]].

> [!info]
> this is difficult to achieve in [[distributed-systems]] due to the tendency to use [[asynchronous-replication]] in order to maintain low [[latency]] in the system.

## Advantages.

- clients and developers can treat a [[distributed-systems|distributed-system]] as a simpler single-node system.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related

- [[consistency]]

Categories:: [[distributed-systems]], [[database|databases]]
