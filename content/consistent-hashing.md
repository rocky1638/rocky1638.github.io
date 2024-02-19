# Consistent Hashing

![[consistent-hashing.png]]
- all of the nodes of the [[distributed-systems|distributed system]] are placed equidistant on a ring and assigned a value by their position.
- we then use a normal hash function that is $\mod L$ where $L$ is the length of the ring.
- data is hashed onto the ring, and is stored on the first node *in front* of where it landed.
	- this way, we get very well spread out data amongst all of our nodes.
- on node failure, we only have to reassign values to the node in front of the one who failed, instead of repartitioning everything.
 - nodes might start having uneven load because when a node is removed, all of its load/data are moved to the next node.
	 - this can be mitigated with [[virtual-nodes]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[database]]
