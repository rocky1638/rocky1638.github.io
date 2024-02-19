---
created_at: 2024-01-26
type: concept
aliases: 
parents:
  - "[[database-index]]"
children: 
supports: 
enemies:
---

# lsm-tree and sstable index

An **LSM tree**, or log-structured merge tree, is a balanced binary search tree in which each node has a key and contains a value. _(This value could be actual data or a memory address, see [[database-index#co-locating data]] for details)._

> [!info]
> LSM trees are typically constructed with data structures like red-black trees or AVL trees.

Just like a [[b-tree-index|b-tree]], each non-leaf node contains ranges along with pointers to children nodes, while each leaf node contains key-value pairs.

Under normal database operation, the entire LSM tree lives in-memory, and new data is written to it in $O(\log n)$ time.

Once the LSM tree grows too large for memory, it is written to disk as an **SSTable**, or sorted-string table and then cleared. An SSTable is simply a list of key-value pairs that are sorted by key.

> [!info]
> The LSM tree is also sometimes called the _memtable_.

## reading from the index

To read, we first binary search the LSM tree. If no results are found, we iterate in reverse-chronological order through the SSTables on disk.

See [[log-based-storage#optimizations]] for details on how SSTable reads and storage are optimized.

## pros

- [p] Can be stored on disk.
- [p] Faster writes than b-trees because we first write to memory.

## cons

- [c] Range queries require searching through LSM tree and all SSTables.
	- This is still faster than hash indexes, because the tree and tables are all sorted.
- [c] Compaction in the background requires extra CPU usage.

## optimizations

### sparse indexes

Now that all of our data is sorted in SSTables, we can have **sparse indexes** over top of each SSTable. This further improves the search of each SSTable to below $O(\log n)$, because we can find a _nearby_ key and linear scan from there.

### bloom filter

TODO: research more into this

## references

- [LSM Tree + SSTable Database Indexes | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=ciGAVER_erw)
