---
type: concept
parents:
  - "[[availability]]"
---

# availability patterns

- two patterns to support high availability.
	- [[failover]].
		- master slave pattern.
			- heartbeats are sent between the active server and the passive server that’s on standby.
			- when the heartbeat is interrupted, the passive server takes over as the active server.
		- active-active (a.k.a. master-master).
			- both servers are running and spreading the load.
		- disadvantages.
			- adds more hardware and complexity.
			- potential for lost data is the active system fails while replicating data to the passive.
	- replication.
		- similar idea to [[database-replication]].
		- [[single-leader-replication]] or [[multi-leader-replication]].
