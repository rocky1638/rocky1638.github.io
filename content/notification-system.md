# Notification System

- the three main types of notifications are push notifications, sms text messages, and emails.
- clarifications.
	- notification system should support all three types of notifications mentioned above.
	- the system should be as real-time as possible, but we can allow for a slight delay when the system is under high demand.
	- notifications can be triggered by client-side applications and directly from the server.
	- users can opt-out of receiving notifications.
	- millions of notifications sent out daily.
- design.
	- to send notifications, we need to store user’s contact information when they download our app or login to our website.
		- these can simply be stored in a database, but of course can have standard scaling strategies applied such as [[database-sharding]] or [[database-replication]].
	- all of our various app services should call a notification service, that is in charge of generating notification payloads that can be sent to third-party providers to actually send emails, texts, etc.
		- these notification servers should be able to be scaled horizontally.
	- we can use [[asynchronism]] and [[message-queue]] to decouple our system components temporally.
	- ![[notification-system-diagram.png]]
	- our various services will call our notification servers through api requests that are only accessible internally.
	- deep dive.
		- we have to make sure notifications aren’t lost, so we can store notification data in a log database.
		- we have unique notification ids, so we can dedupe our notifications in case our distributed system tries to send it twice.
		- we can integrate [[rate-limiter]] on our side to satisfy our users’ notification settings.
		- we could look into keeping track of notification open and clickthrough rate.
- ![[notification-system-diagram-with-auth.png]]
	- here’s the diagram now with authentication and rate-limiting in the notification servers.
	- we also now have a retry mechanism on the workers and [[message-queue]].

Categories:: [[system-design]]