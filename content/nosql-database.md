---
type: concept
parents:
  - "[[database]]"
aliases:
  - nosql
---

# nosql databases

- data represented in a key-value store, document store, or graph database.
- data is [[denormalization|denormalized]].
- joins are done in application code.
- favors [[eventual-consistency]].
	- in terms of [[cap-theorem]], nosql favors [[availability]] over [[consistency]].

## types of nosql databases

### key-value store

- basically a hashmap.
- backed by memory, and allows for $O(1)$ reads and writes.
- keys can be maintained in order.
- often used for [[caching]].

### [[document-database]]

### [[graph-database]]

### wide column store

![](https://github.com/donnemartin/system-design-primer/raw/master/images/n16iOGk.png)
- basically a nested hashmap.
- examples include bigtable, hbase, and [[cassandra]].
- high availability and high scalability.
- normally used for very large datasets.

## references

- https://en.wikipedia.org/wiki/Key-value_database
