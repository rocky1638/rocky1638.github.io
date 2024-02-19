---
title: "hash index"
created_at: 2024-01-26
type: concept
aliases: 
parents:
  - "[[database-index]]"
children: 
supports: 
enemies:
---

![[hash-map-diagram.png|Figure 1: A diagram of a basic hashmap.|650]]

In-memory, we can store a key-value pairs of keys with addresses/data.

![[hash-index.excalidraw|100%]]

This allows us to achieve amortized $O(1)$ time with lookups in this hash table, pointing us to the address where the data we want to find is on disk.

> [!attention] A word on hashing
> Because of hashing, there's no guarantee that similar keys are close to each other on disk!

## pros

- Reads to the hash map are very fast, as they are in-memory and don’t require disk I/O.

## cons

- The hash map must be maintained in-memory, because implementing a hash map on disk requires lots of random disk I/O.
- All of our keys need to fit into memory.
- RAM is not [[durability|durable]].
- Range queries are not possible in under $O(n)$ time, because the hash map doesn’t implicitly store information about how keys are related to each other (unlike [[b-tree|b-trees]]).

## references

- [How do Hash Indexes work? | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=I1wQsY-Nh_k)
