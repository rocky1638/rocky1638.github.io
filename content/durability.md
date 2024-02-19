---
created_at: 2022-12-31
type: concept
aliases: 
parents:
  - "[[acid-transactions]]"
---

# durability

- a guarantee that once a transaction is committed, it will persist even in the event of a failure.

## In a non-distributed context.

- [[database-transaction|transactions]] and their effects are stored in some non-volatile storage.

## In a distributed context.

- [[database-transaction|transactions]] should be durable stored in multiple nodes in the event of [[partial-failures]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```
