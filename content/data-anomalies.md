---
created_at: 2022-12-31
type: concept
aliases: [data-anomaly, anomaly, anomalies]
---

# Data Anomalies

- errors that can occur within [[database|databases]] when [[database-transaction|transactions]] are not [[isolation|isolated]] properly.
- especially relevant in [[distributed-systems]] with [[concurrency|concurrent]] operations.

## Types of data anomalies.

- dirty write.
	- when two write operations run in sync and we end up with a mish-mash of their values.
	- very difficult to roll-back.
- dirty read.
	- when an operation reads a value from another uncommitted operation.
- fuzzy read.
	- a value retrieved twice during an operation is different on both retrievals.
- lost update.
	- when two operations try to update the same value, but only one operation wins, while the other one isn’t aware of anything going wrong.
	- ![[data-anomalies-diagram.png]]
- read skew.
	- when one operation alters and then commits some data that is needed to be read by another ongoing transaction.
	- ![[read-skew-diagram.png]]
- write skew.
	- when two operations read the same data but then modify different data.
	- ![[write-skew-diagram.png]]

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[isolation]]
- [[asynchronism]]

## References.

Categories:: [[database]]
