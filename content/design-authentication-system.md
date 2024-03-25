---
title: "design authentication system"
tags:
aliases: 
parents: 
children: 
supports: 
enemies:
date: 2022-12-30
updated: 2024-03-23
---

## my solution

### functional requirements

- User should be able to create a new account with an email and a password.
- User should be able to log in with email and password.
- User should receive a cookie/token that allows them to login for a set amount of time without entering details.
- User should be able to logout.

### non-functional requirements

- Available, users should always be able to log in.
- Consistency.
	- If a user changes a password, the old password should most definitely stop working!
- Should scale to a large scale, 100M users+.
- Read heavy - more people are likely to login vs. creating new accounts.

### api requirements

- `createAccount(username: str, password: str)`
- `login(username: str, password: str)`
- `login(sessionToken: str)`
- `logout(sessionToken: str)`

### db design

![[design-authentication-system-db.png]]

### design process

Starting with a single machine, let’s look at the create account flow.

![[design-authentication-system-create-account.png]]

The login flow doesn’t add much complexity. We just check the username and password against our database.

If the login is successful, we generate a unique session token using values such as the user’s email and the current timestamp, as well as a hashing function like SHA256 (we can then do something like hex or base64 encoding based on length requirements).

Then, we send that back in a SET-COOKIE header, which the user’s browser stores for subsequent queries.

This will work until our authentication service will no longer be able to handle that amount of concurrent requests. To scale our authentication servers and remove the SPoF, we can horizontally scale these servers as they are atateless, and add a load balancer in front.

![[design-authentication-system-2.png]]

Now, our database won’t scale alongside our servers, if more requests are coming in for reads and writes. We can shard our database by some key like our users geography, or their emails. Regardless, this way, we can split out our database into multiple distinct machines.

Furthermore, because we will need to check all the authenticated requests of every API call for every user, our DB will field many requests to the `sessions` table. Due to the high read nature of this, as well as the ephemeral nature of the session token, we can consider storing this data in a cache.

This has the added benefit that if the cache goes down, we don’t care too much about durability as a user can just log in again.

> Another option that I can think of is to store session tokens in the memory of auth service server machines, and have the load balancer keep track of the mapping between a users’ active session and which machine they should interact with.

![[design-authentication-system-sharded.png]]

Still now, if we expect there to be many more users logging in vs. creating new accounts, we could also create read replicas on our sharded databases.

However, for consistency reasons, we want to make sure that for a period of time after a user is created or a password is updated, we run reads through the leader nodes, so that we don’t log in a user with an old password.

## positive feedback

- Use of a distributed cache to store session tokens is a valid strategy.
- Method of generating unique session tokens using a hashing strategy plus a random salt was valid and a good idea.
-

## critique

- Should have talked about the trade-offs between using cookies and bearer tokens (JWTs) for authentication.[^1]
	- Both of these things are used to send data in a HTTP header.
	- Cookies:
		- Formally, is just a text header that can be used to send anything.
		- They have an associated domain and expiry date.
		- They are automatically sent with all requests to their respective domain.
			- This opens up the possibility of CSRF and XSS attacks.
	- Bearer token:
		- Usually in the form of a JWT or JSON web token, these can be stored/passed along as a cookie as well, or the web application can put it into local storage, and the app can manually send this along with every request.
- Could have discussed the possibility of refreshing access tokens.

## references

- [Design Authentication System](https://www.youtube.com/watch?v=uj_4vxm9u90)

[^1]: The post [here](https://stackoverflow.com/a/38470665) describes the difference between the two quite well.
