---
created_at: 2022-11-26
type: concept
aliases: []
---

# cap theorem

> [!warning] Disclaimer
> The CAP theorem, although useful to illustrate a point about distributed systems, is seen today as an oversimplification of trade-offs and considerations when designing systems.
>
> For example, it fails to mention latency when choosing consistency guarantees, and failure modes such as network delays and dead nodes when considering fault tolerance.
>
> I’m leaving this page here for now, but I wouldn’t read too much into it.

The CAP theorem forces us to make tradeoffs between [[availability]] and [[consistency]].

## the three pillars

- [[consistency]].
	- a read is guaranteed to generate the most recent write.
- [[availability]].
	- a non-failing node will return a reasonable response within a reasonable amount of time *(not necessarily a consistent response, if consistency isn’t guaranteed).*
- Partition tolerance.
	- the system will still work if some partitions go down and become unreachable.
	- inevitable with [[partial-failures|partial-failure]].

## the three possible choices for any distributed system

![[cap-theorem-diagram.png]]

> [!info]
> A distributed system can either be consistent or available in the presence of a [[network-partition]].

- CP - consistency and partition tolerance.
	- requests might time out, but if they don’t, are guaranteed to be the most updated value.
	- good if the business requires atomic reads and writes.
- AP - availability and partition tolerance.
	- requests always return the most readily available data, but it might not be the latest.
	- writes might take some time to propagate, great for [[eventual-consistency]].
- CA - consistency and availability.
	- we can ensure this only if we don’t have partition-tolerance, which is not very useful if we want a good distributed system.

## references

- https://robertgreiner.com/cap-theorem-revisited/
- http://ksat.me/a-plain-english-introduction-to-cap-theorem
