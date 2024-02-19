---
created_at: 2022-12-31
type: concept
aliases: 
parents:
  - "[[database-transaction]]"
supports:
  - "[[consistency]]"
---

# Isolation

- a guarantee that even though [[database-transaction|transactions]] might run [[concurrency|concurrently]], the result will always be as if the operations ran one at a time.
- we want to prevent [[data-anomalies]].

## Isolation levels.

- [[serializability]].
- [[repeatable-read]].
- [[snapshot-isolation]].
- [[read-committed]].
- [[read-uncommitted]].
