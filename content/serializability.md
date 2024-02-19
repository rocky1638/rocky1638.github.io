---
created_at: 2022-12-31
type: concept
aliases: 
parents:
  - "[[database]]"
  - "[[distributed-systems]]"
---

# Serializability

- two [[database-transaction|transactions]] executed [[concurrency|concurrently]] should produce the same result as if they were run sequentially.
- this is the strongest level of [[isolation]].
- leads to [[strict-serializability]] when combined with [[strong-consistency|linearizability]].
