---
created_at: 2024-01-26
type: concept
aliases: 
title: "relational databases"
parents:
  - "[[database]]"
enemies:
  - "[[nosql-database]]"
---

a database in which data is stored in tables, and complex queries can be made through joining of the tables based on unique primary and foreign keys.

## pros

- they allow for many-to-many and many-to-one relationships.
- querying through sql is declarative and easy to understand.
- there is often [[normalization]], where we refer to shared values by an id and then save the actual value in one place.

## cons

- a downside is that there is often a translation layer between the db (of rows from various tables), to the application layer (unified data).
	- this is called [[impedance-mismatch]].
