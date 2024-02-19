---
created_at: 2022-12-31
type: concept
aliases: []
---

# Atomicity

- a guarantee that either all operations are completed, or none are.
	- essentially the promise that a [[database-transaction]] gives.
- in [[distributed-systems]], a system might need to perform the same operation in multiple nodes.
	- we’d want either all of the nodes to do the operation, or none of them.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[database]]
