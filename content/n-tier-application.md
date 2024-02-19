---
created_at: 2023-01-12
type: concept
aliases: []
---

# N-Tier Application

- an application that has more than three components on separate machines.
- essentially all apps built with [[microservices]] will be classified as this type of application.
	- these components can include [[caching]], [[message-queue]], [[load-balancer]], etc.
- all large-scale consumer applications have more than three tiers.

## Why so many tiers?

- we want to maintain two key [[software-design-principles]]:
	- [[single-responsibility-principle]].
	- [[separation-of-concerns]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[microservices]]
