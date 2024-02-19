---
created_at: 2022-11-26
type: concept
aliases: [consistency-models]
---

# Consistency Patterns

- these models define the valid set of execution histories in a [[distributed-systems|distributed-system]].
- they help us to formalize the behavior and safety promises of these systems.
- a consistency pattern is considered **stronger** if it allows less possible histories, and usually makes it easier to build an application on top of it.

## The three main patterns.

- [[strong-consistency]].
- [[causal-consistency]].
- [[eventual-consistency]].
- [[weak-consistency]].
	- after a write, reads may or may not see it.
	- used in [[memcached]].
	- useful in video chat, phone calls, etc.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[distributed-systems]]
