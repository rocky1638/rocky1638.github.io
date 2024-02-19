---
created_at: 2023-11-10
type: book
title: "designing data intensive applications by martin kleppman"
aliases:
  - ddia
---

## chapter 1 - reliable, scalable, and maintainable applications

[[whats-the-point-of-system-design-anyway]]

## chapter 2 - data models & query languages

This chapter covers the three main types of databases and their trade-offs.

- [[relational-databases]]
- [[nosql-database]]
	- [[document-database]]
	- [[graph-database]]

## chapter 3 - storage and retrieval

This chapter covered various concepts related to storing and retrieving data efficiently, including:

- [[log-based-storage]]
- [[database-index]]
	- [[hash-index]]
	- [[b-tree-index]]
	- [[lsm-tree-and-sstable-index]]

It also covers the differences between **OLAP (online analytical processing** and **OLTP (online transactional processing)**, and how that affects the ways in which we store data.

OLAP workflows typically retrieve a few columns from many rows in a table *(think grabbing the average order price for all payments made through Shopify)*. Because of this, it can make sense to store data by column on disk, instead of by row. Furthermore, there’s normally many less distinct values in a column than their are rows in a column, meaning compression methods such as **run-length encoding (RLE)** become viable.

On the other hand, OLTP workflows (typical user behavior) require fast reads and writes to individual rows.

## chapter 4 - encoding and evolution

Last chapter focused on how data is stored, and this chapter follows with *the format* in which this data should be stored.

For this, data needs to be encoded and decoded. See [[data-encoding]].

### transfer layer

This chapter also briefly touches on how encoded data is transfered.

#### database

The application encodes in-memory data to store on the database. In turn, the application decodes data from the database to load into memory.

#### rest (representational state transfer)

REST is a stateless, resource-based transfer protocol that accepts HTTP requests and returns data in popular formats like JSON and XML.

1. The sender encodes their request.
2. The server decodes the request.
3. The server encodes a response.
4. The sender decodes the response.

#### rpc (remote procedure call)

A call to a function whose implementation is on another node.

Requires an intermediary RPC client that can serve as a middleman to encode/decode requests and responses between the two services *(because the two services likely don’t understand each other’s formats)*.

Because of this, it’s typically used for communication between internal services (like datacenters).

Custom RPC protocols like gRPC use more efficient encodings such as Protocol Buffers.

## chapter 5 - replication

This chapter first focuses on the reasoning behind [[database-replication]], and the various strategies that can be used.

- [[single-leader-replication]]
- [[multi-leader-replication]]
- [[leaderless-replication]]

Then, in the context of multi-leader and leaderless replication, the author discusses strategies for conflict resolution.

### consistency guarantees

- read-your-writes / read-after-write consistency
	- ![[read-after-write-consistency-diagram.png]]
	- a user will always see writes submitted by themselves.
		- many strategies for this
			- user reads from leader for 1 minute after latest submitted update
			- user only reads from followers <1minute behind leader
			- read data only changeable by the user from leader
- monotonic reads
	- ![[monotonic-reads-diagram.png]]
	- don’t want to move backwards in time
	- stronger than eventual consistency
		- user always reads from one replica - what happens if the replica fails?
- consistent prefix reads
	- this issue only happens once partitioning/sharding is done
	- with only one leader there is a consistent global ordering

### conflict resolution

- concurrent writes
	- ![[concurrent-writes-diagram.png]]
		- last write wins
			- [c] loss of durability as some writes may be discarded silently
		- how to keep track of causal dependencies?
			- ![[causal-dependency-diagram.png]]
			- version each key
				- on read, server returns all values not yet overwritten and latest version number for key
					- application must perform merge/conflict resolution of varying versions received here
				- on write, client includes version number of prior read
				- db can overwrite all values of key with version number of prior read and below
				- in leaderless:
					- use version vector, where each value has a version for each replica
