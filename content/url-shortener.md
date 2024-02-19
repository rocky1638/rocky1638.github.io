---
created_at: 2022-12-08
type: system-design-example
aliases: []
---

# URL Shortener

- clarifying questions.
	- 100 million urls generated per day.
		- approximately 1160 urls generated per second.
		- assuming reads are 10 times more common than writes, that’s 11,600 reads per second.
		- assuming the service will run for 10 years, we will need to store about 365 billion records.
		- assuming average url is 100 bytes, we need to be able to store 365 TB of data.
	- shortened url is as short as possible.
	- shortened url can contain numbers and letters.
	- assume shortened urls cannot be updated or deleted.
	- high availability, scalability, and fault tolerance.
- design.
	- in terms of a rest design, we will redirect the short urls to the full url using a 301 redirect.
		- this 301 redirect is a permanent redirect, meaning that the browser will cache the result and not hit the tinyurl server on subsequent calls.
	- the easiest way to map these short urls to long urls would be to use a hash table.
		- we need a good hash function.
	- a hash table is not scalable to a real-world distributed system, so we should use a relational database instead.
	- hashing function.
		- we can use a standard hashing function and then use a predefined suffix string to deal with collisions.
			- fixing collisions can be time consuming.
		- we can use modulo math to create unique ids based on the ids of the long urls in the database.
			- it is easy to figure out the tinyurl id, which can be a security concern.
			- we have to consider how to generate unique ids in a distributed system.
	- because reads happen more often than writes, we can cache the database values.
	- further thoughts.
		- add a rate limiter to prevent malicious actors.
		- easy to scale the web tier because it is stateless.
		- possiblity to scale the database.

Categories:: [[system-design]]
