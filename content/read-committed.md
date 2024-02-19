---
created_at: 2022-12-31
type: concept
aliases:
---

# read committed

Read committed isolation is an isolation level that promises to stop both **dirty reads** and **dirty writes**.

A dirty read occurs when Bob reads a value that Alice is in the process of writing, before she has committed the transaction.

A dirty write occurs when Bob writes to a value that Alice has written to, but has not yet committed. This causes Alice’s value to be overwritten.

## references

- [Read Committed Isolation | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=oS60pr8H1e0)
