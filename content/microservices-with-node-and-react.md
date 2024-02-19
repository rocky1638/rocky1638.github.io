# Microservices with NodeJS and React with Stephen Grider

- We want to use microservices to split up our monolithic architectures into separate services that are each only responsible for one thing.
	- Each of these services should also read and write to their own databases.
- This brings up issues with dependencies when some business logic or use case requires data from the databases of two other services.
- The solution here is to have two microservices talk to each other.
	- This can be done either synchronously or asynchronously.
	- Sync communication lets services talk directly to one another, but can introduce long chains of dependencies which ultimately increase chance of failure and latency.
	- Async communication can be done using [[message-queue]].
		 - We can create a shared event bus that all our services access.
			 - Services can emit events to the event bus, which are then accessed by the other services to return required information or perform requested operations.
			 - This is bad because it introduces a single point of failure, and still has the same downsides of synchronous communication when one of the services goes down.
		- We can keep using an event bus, but instead of direct one-to-one events, we use a notify-subscribe pattern.
			- Have each service store all the data they will need to do their job.
				- Note that each service might not be responsible for taking user input and updating this data directly…
					- Have all services emit events whenever something interesting occurs *(object created, updated, deleted)*.
			- Any interested services can subscribe to the types of events that they care about, and do whatever they want with the information emitted by these other services.
			- Pros.
				- Services that require information from other services no longer depends on these other services to be running!
			- Cons.
				- Data is duplicated across multiple services.
					- This is not really an issue because nowadays, storage is the cheapest thing we can scale.
- Deep dive into events.
	- Events have no set structure, but are used to sent pieces of data.
	- There are prebuilt event buses such as RabbitMQ and Kafka.
	- Our services post to the event bus, and the event bus will echo these events as POST requests to all of our services.
- [[microservices-toy-blog-app-stephen-grider]]
- [[docker]] & [[kubernetes]].
	- Kubernetes puts these containers into nodes, and then provides a master that handles communication between these nodes, as well as scaling and node health.
		- Provides a common communication channel.
- Skaffold.
	- Automates many tasks in a [[kubernetes]] dev environment.
	- Can update code in a running pod.
	- Start with `skaffold dev`.
- [[microservices-ticketing-app]]

Categories:: [[microservices]]
