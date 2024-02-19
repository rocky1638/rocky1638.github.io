---
created_at: 2022-12-28
type: concept
aliases: [partial-failure]
---

# Partial Failures

![[partial-failures.png|700]]

- this is particularly an issue in distributed systems when only some nodes fail, because then data and operations can get out of sync between nodes.
- because nodes can fail at any time, some messages may be sent multiple times, never at all.
	- see [[exactly-once-semantics]].
- failing nodes are typically detected through implementing some form of [[timeout]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

Categories:: [[availability]]
