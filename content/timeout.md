# Timeout

- we set a timeout value to continuously check nodes to see if they are up and running.
- there are tradeoffs for short and long time outs.
	- if we have a short time out, we detect failures faster, but some nodes might be declared dead when instead they are just a bit slow, leading to false positives.
		- ![[false-positives.png]]
	- if we have a long time out, we will identify crashed nodes slower, but will be more lenient with slow nodes.
		- ![[false-negatives.png]]

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[distributed-systems]]