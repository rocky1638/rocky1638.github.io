---
title: "document database"
created_at: 2024-01-26
type: concept
aliases: 
parents:
  - "[[nosql-database]]"
---

- centered around documents such as [[json]], XML, binary, etc.
- have apis that allow querying based on the internal structure of the documents.
- examples include [[mongodb]] and [[couchdb]].
- provide high flexibility and typically used for data that occasionally changes.
- quite similar to key-value stores because key-value stores often also allow for the storing of metadata.

## pros

- [p] schemas are typically not explicitly defined at write-time, so they are enforced by the application code at read-time.
- [p] better [[locality]], because data is [[denormalization|denormalized]].
	- this, in turn, leads to better performance when compared to [[relational-databases]].

## cons

- [c] depending on how documents are stored, any change might require a complete rewrite of the document on the disk.
- [c] support for joins (especially many-to-many relationships) is weak _(this goes hand-in-hand with denormalization)._

## use-cases

- applications that don’t require many-to-many relationships.
	- i.e. an analytics applications that just records events.
