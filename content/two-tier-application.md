---
created_at: 2023-01-12
type: concept
aliases: []
---

# Two Tier Application

- an application that involves a client and a server.
	- the client includes the user interface and some business logic.
	- the server contains the [[database]].

## Advantages.

- some business logic can be contained on the client side to reduce the impact of network [[latency]].
	- we maintain more control over our app by keeping sensitive and important information away from the access of the user on our server.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[single-tier-application]].

## References.

Categories::
