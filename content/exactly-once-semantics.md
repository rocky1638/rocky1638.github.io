# Exactly-Once Semantics

- in [[distributed-systems]], we want nodes to process every message that needs processing exactly once, not too few and not too many times.
- if nodes do not retry when their message isn’t acknowledged, they could potentially miss out on completing the delivery of a message.
	![[message-not-delivered.png]]
- if nodes retry too much, they might send the same message too many times.
	![[message-delivered-twice.png]]
- one way to solve this issue is to have the application code on the receiving node do [[deduplication]] to ensure that even if it receives multiples of the same message, it only shows one to the user.
	- so, we can have sent messages be **at-least-once** and receiving nodes to accept **at-most-once.**
 - **exactly-once processing** is possible in [[distributed-systems]], but exactly-once delivery is not.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[distributed-systems]]