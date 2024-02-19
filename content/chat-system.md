# Chat System

- clarifications.
	- supports both 1-on-1 and group chats with groups as big as 100 people.
	- supports fifty million daily active users.
	- text only.
	- message size limit of 100,000 characters.
	- store chat history forever.
- high level design.
	- our clients will communicate with a chat service that then relays these messages to a recipient.
	- websocket connections are used for establishing two-way communication between a client and a server so the server can send new messages whenever it sees fit.
		- websocket is essentially an upgraded http collection.
	- only the chat portion of the system needs to use websocket.
		- everything else can remain with http requests.
	- everything else such as logging in and user profiles can be stateless web architecture.
	- push notifications can be a third party service, see design ideas for that in [[notification-system]].
	- ![[chat-system-diagram.png]]
		- we also maintain real-time presence servers that keep track of users’ online/offline status.
		- also need big databases to store user chat history.
			- this can be stored in a simple key-value store that is keyed by a unique user identifier.
			- examples include hbase or cassandra.
- deep dive.
	- we can use a service discovery tool like apache zookeeper to send user requests to the closest chat server near them so that the latency is low.
	- presence servers use a heartbeat system to set users to offline after they miss a certain number of heartbeats.
		- presence servers keep track of status and last active time in a key value store.
	- 1-on-1 chatting.
		- two users are each synced up to a chat server.
			- one user’s messages are sent to a message queue, saved in a key value store, and then either sent to a notification system or directly to the other user’s chat server.
	- group chats.
		- one user’s messages can be sent to multiple message queues.
		- on the recipient side, a user’s message queue accepts incoming jobs from multiple other users who are in the group chat.

Categories:: [[system-design]]
