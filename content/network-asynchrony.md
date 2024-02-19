---
created_at: 2022-12-28
type: concept
aliases: []
---

# Network Asynchrony

- the idea that networks cannot provide strong guarantees that events will arrive to another node in the network in order, or in a timely manner.
- also can be an issue when different nodes run on their own clocks, which might run at slightly different rates.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[asynchronism]], [[networking]]
