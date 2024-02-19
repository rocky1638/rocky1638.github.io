---
created_at: 2022-12-31
type: concept
aliases: []
---

# Causal Consistency

- we only guarantee that reads that directly rely on each other, such as comment responses, appear in order.
	- separate comment chains, for example, can be shown in different orders to different users.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[consistency-patterns]]
- [[asynchronism]]

## References.

Categories:: [[distributed-systems]]
