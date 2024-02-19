---
created_at: 2024-01-26
type: concept
title: "normalization"
aliases: 
parents:
  - "[[relational-databases]]"
enemies:
  - "[[denormalization]]"
---

- the process of abstracting away data when it’s referenced multiple times.

## pros

- if we need to make an update to the normalized value, we only need to change the value in one place.
	- i.e. updates to the normalized value are constant time.
- we don’t need to worry about values getting out-of-sync with each other.

## cons

- we now need to join against another table to retrieve normalized values.
	- the more data is normalized, the more [[locality]] is reduced.

> [!example]
> imagine we have an app like uber eats where users and restaurants all need to have an address which includes a state.
>
> instead of storing the string “NY” or “CA” in every place we needed to store a state, we would store the string “NY” in a single location, and then just reference the location, or id of that string in all other places where we needed it.
