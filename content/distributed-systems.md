---
created_at: 2022-12-28
type: moc
aliases: [distributed-system]
---

# distributed systems moc

TODO: clean up after i get all my old files wrangled

A distributed system is a computer system in which multiple machines, linked by a network, work together to serve an application to users.

## what makes a good distributed system?

Ideally, we want the end user to be completely oblivious to the fact that multiple machines are handling their requests.

Done right, a distributed system should, to the end user, feel the same as interacting with a single machine. To this end, the [[atomicity]], [[consistency]], and [[isolation]] are all necessary to ensure no weirdness happens on the users’ end.

A good distributed system should also be [[durability|durable]].

## why are distributed systems hard to build?

Many issues arise when trying to keep multiple machines in sync across an unreliable network.

- [[network-asynchrony]]
- [[partial-failures]]
- [[concurrency]]

### failure modes

- **Fail-stop**: A node stops and remains stopped, and other nodes know that it has stopped because communications remain open.
- **Crash**: A node silently stops, and other nodes can only guess that it has failed through communications.
- **Omission**: A node stops responding to incoming requests.
- **Byzantine**: A node starts doing random stuff, likely due to bugs or malicious actors.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```
