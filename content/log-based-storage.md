---
created_at: 2024-01-26
type: concept
aliases:
parents: 
children: 
supports: 
enemies:
---

# log-based storage

Stores key-value pairs in a long log file, which is appended to when any new data is added.

---
At its most basic, this kind of non-relational database could be implemented in as little as two bash commands:

```bash
#!/bin/bash

db_set () {
	echo "$1,$2" >> database
}

db_get () {
	grep "^$1," database | sed -e "s/^$1,//" | tail -n 1
}
```

> [!hint]
> Updates to a key are also appended! That's why when we `get` a key, we look for the newest instance of that key.

## pros

- [p] Writes will always be $O(1)$ because all we’re doing is appending to the end of a file.

## cons

- [c] Reads become $O(n)$ and very slow as the log grows.
	- To improve performance, we need to use [[database-index|indexes]].

## optimizations

- To prevent hash indexes from getting too large and not being able to fit in memory, we can break up logs into fixed size chunks.
 - To improve the space and read efficiency of log based storage, we can use compaction and merging.

![[compaction-merging-diagram.png|an example of a log that was compacted and then merged]]

- Compaction is the act of deleting old value of keys in the log that have now been updated.
- Merging is done after compaction, if the newly compacted data from two sections are now small enough to fit in one fixed-size block.
