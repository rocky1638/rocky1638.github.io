---
created_at: 2022-12-08
type: system-design-example
aliases: []
---

# Distributed Unique ID Generator

- clarifying questions.
	- ids must be unique and sortable.
	- ids are only numerical values.
	- ids should fit into 64 bit.
	- system should generate 10,000 IDs per second.
- possibilities.
	- scale `id` values by `k` where `k` is the number of servers.
		- disadvantages.
			- this does not scale well when we want to add or remove servers.
	- generate unidue uuid’s of 128bit length, very unlikely to have a collison.
		- disadvantages.
			- these ids cannot be sorted by time of creation.
			- they contain values that are not numeric.
	- have a single server that generates ids for each of the distributed servers.
		- disadvantages.
			- single point of failure.
	- ![[distributed-unique-id-visualization.png]]
		- we can create custom ids by mixing a bunch of various ids including the timestamp, datacenter id, machine id, and a sequence number that is incremented with each id and reset every millisecond.
- deep dive - twitter snowflake approach.
	- by using a timestamp at the beginning, our ids can be sorted by time.
	- by using data center and machine ids, we avoid collisions in a distributed system.
	- we use the last 12 bits for generating a sequence number, to help distinguish ids that are generated on the same timestamp.
	- advantages.
		- high availability because no servers depend on any servers to run, so single point of faliure.
		- ids can be sorted by time created.

Categories:: [[system-design]]
