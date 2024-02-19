# Database Partitioning

- databases can be partitioned either horizontally or vertically.
- when we partition vertically, we split up the data by their columns.
	- this can make it difficult to access all the data we need while working in a [[distributed-systems]].
- when we partition horizontally, we split up entire rows of data into different physical databases.
	- it can be harder to perform atomic operations when we partition horizontally, because the data we are changing might be spread out over multiple nodes.
	- this is more commonly known as [[database-sharding]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[database]], [[distributed-systems]]
