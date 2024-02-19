---
created_at: 2022-12-31
type: concept
aliases: []
---

# Read Uncommitted

- a transaction can read uncommitted data by another transaction.
- this is the weakest level of isolation.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[isolation]], [[database]]
