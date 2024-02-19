# Denormalization

- improve read performance at the expense of write performance.
- write redundant copies of data to multiple tables.
	- this allows most complex join operations to be avoided.
		- this is important because when we split up our databases with [[database-sharding]] or [[database-federation]], joins become more difficult to do.
- disadvantages.
	- duplicated data.
		- redundant data needs to be kept in sync.
	- slow writes.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

- https://en.wikipedia.org/wiki/Denormalization

Categories:: [[database]]
