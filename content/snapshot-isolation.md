---
created_at: 2022-12-31
type: concept
aliases: []
---

# snapshot isolation

![[snapshot-isolation-diagram.png|Figure 1: How various transactions read a column value under snapshot isolation.]]

Snapshot isolation is a form of database isolation where values in a database are versioned by transaction numbers.

Thus, when a user makes a read from the database, they see a *consistent snapshot* of that database at any given time. This is especially useful if a large read query needs to make sure that data doesn’t get changed out from under it as it’s doing the read, also known as **read skew**.

From the diagram above, you can see that any transaction will only use the state of the database from before it started, ignoring any changes that have been made by transactions that started after it!

## references

- [Snapshot Isolation | Systems Design Interview: 0 to 1 with Google Software Engineer](https://www.youtube.com/watch?v=Tgpa9TrxsfU)
