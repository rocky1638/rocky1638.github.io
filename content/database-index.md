---
title: "database index"
created_at: 2024-01-26
type: concept
aliases:
  - index
parents: 
children: 
supports: 
enemies:
---

Additional data structures that are used by [[databases]] to improve the performance of reads on a specific key value at the expense of slowing down writes.

---

## types of index data structures

- [[hash-index]]
- [[b-tree-index]]
- [[lsm-tree-and-sstable-index]]

### trade-off analysis

| Type of index       | Read Performance | Write Performance | Range Query?                                                                                          | Storage          |
| ------------------- | ---------------- | ----------------- | ----------------------------------------------------------------------------------------------------- | ---------------- |
| Hash index          | $O(1)$           | $O(1)$            | $O(n)$                                                                                                | in-memory        |
| B-tree              | $O(\log n)$      | $O(\log n)$       | $O(\log n + m)$, where $n$ is the size of the tree and $m$ is the size of the dataset returned        | disk             |
| LSM tree + SSTables | $O(\log n)$      | $O(\log n)$       | $O(\log (n+mx))$, where $n$ is the size of the tree and $mx$ is the total size of all of the SSTables. | in-memory + disk |

## recovering from faults

All the indexes listed above can make use of **write-ahead logs (WALs)** to ensure that faults don’t cause dropped writes.

A write-ahead log is used as so:
1. A write needs to be made into the index.
2. Before writing anything to the index, a record is appended to the WAL.
3. The write is made to the index.
4. If the write is successful, we “cross off” the record in the WAL.
5. If the system crashes before the write completes, the system will first complete any incomplete operations in the WAL before moving on to new write requests.

## co-locating data

Indexes contain key-value pairs; the values in these pairs can either be the actual data, or just a pointer to the data.

The three methods here include:

1. **Clustered index**: The index stores the actual data.
2. **Non-clustered index**: The index stores pointers to the data.
3. **Covered index**: The index stores mostly pointers, but keeps data for some commonly accessed keys.

In general, a clustered index sacrifices storage efficiency in favor of faster reads.

Non-clustered indexes are more common in real-life use cases because we often have multiple indexes. If we used clustered indexes, we’d have to duplicate all of the data.

## multi-dimensional indexes

Indexes can be created based on multiple columns.

For example, we could index on both `name` and then `date`. Everything stays the same, but we’d just sort with `name` as a priority and then tiebreak with `date`.

## references

- [Indexes Concluded | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=QO7KTO-8RWM&list=PLjTveVh7FakLdTmm42TMxbN8PvVn5g4KJ&index=6)
