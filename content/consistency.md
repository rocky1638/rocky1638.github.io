---
created_at: 2022-12-29
type: concept
aliases: [consistent]
---

# Consistency

## In the context of distributed systems.

- a measure of how consistent a system is when it comes to accessing data, in terms of producing the most recent and correct data.
- a definition popularized by the definition for [[cap-theorem]].
- follows several main [[consistency-patterns]].
	- when talking about consistency in the context of [[cap-theorem]], we typically mean [[strong-consistency|linearizability]].
- can be challenging to achieve in a system due to [[network-asynchrony]].

## In the context of databases.

- guarantee that operations only move the database from one valid state to another.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[distributed-systems]], [[database]]
