---
created_at: 2022-12-31
type: concept
aliases: []
---

# Repeatable Read

- data read in a transaction will not change through the duration of the [[database-transaction|transaction]].

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[isolation]], [[database]]
