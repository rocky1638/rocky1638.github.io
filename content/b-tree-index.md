---
title: "b-tree index"
created_at: 2024-01-26
type: concept
aliases:
  - b-tree
parents:
  - "[[database-index]]"
children: 
supports: 
enemies:
---

We store a tree in memory, in which each node of the tree is a disk **page** of fixed size.

Each non-leaf page contains pointers to its children, which are narrowed-down pages. In this way, we can exponentially shrink the search space, achieving logarithmic time to reach any search.

![[b-tree-diagram.png|Figure 1: An example of looking up a key in a b-tree.]]

## pros

- Can be stored on disk.

## cons

- Navigating between pages involves jumping around on the disk (lack of locality).
	- This is still much faster than $O(n)$ sequential scans as datasets increase in size.
- Writing new datapoints can be complicated, as it can requiring fixing-up if the new datapoint causes a page to be split.
	- We will have to split upwards until we reach a page with free space _(this is because a single pointer which used to reference one child page now needs room for two pointers to reference two children)._

## references

- [How do B-Tree Indexes work? | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=Z2OaqmxiH20)
