---
created_at: 2022-12-30
type: concept
aliases:
  - functional-partitioning
parents:
  - "[[database]]"
  - "[[scalability]]"
---

# Database Federation

- also known as “functional partitioning”.
- split up databases by function.
	- e.g. separate databases for users, forums, and products.
	- results in less read and write traffic to each database.
	- smaller databases mean more data can fit in memory, resulting in a higher cache-hit rate.
	- can parallelize writes to these multiple databases.
- disadvantages.
	- not effective if you require huge tables.
	- added complexity in application for determining which database to write to.
	- joining data becomes harder.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```
