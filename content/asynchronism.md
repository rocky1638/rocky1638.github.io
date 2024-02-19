# Asynchronism

- reduce request times for expensive operations by promising to do them later, so that the actual request can finish.
- can also be used to precompute values ahead of time, such as encoding videos or generating thumbnails.
- [[message-queue]].
	- a queue to receive, hold, and deliver messages.
	- application pushes a job request to the queue, and will notify the user of job status and updates.
	- a worker picks up the job from the queue, completes the request, and signals to the user that the job is complete.
	- while the job is enqueued, we can show the end user a temporary local version until the job is actually finished.
	- popular tools:
		- [[redis]] can be used as a simple [[message-queue]] but messages may be lost.
		- [[rabbitmq]].
		- [[amazon-sqs]] is popular but has high latency.
- [[task-queue]].
	- receive tasks and related data, run them, and then deliver the results.
	- very similar to the [[message-queue]], but the tasks on a task queue specify what needs to be done, whereas a [[message-queue]] simply stores messages that workers will read.
	- popular tools:
		- [[celery]].
- [[back-pressure]].
	- when queues grow to be larger than memory, requests start getting dropped because they can’t be stored in memory.
	- we tell users that a server is busy to create pressure for these requests to slow down, so our queue can catch up.
- disadvantages.
	- adds complexity.
	- when it’s just simple usecases, or when there’s not enough requests, synchronous operations without queues might just make more sense.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

- [[asynchronous-replication]]

## References.

Categories:: [[scalability]]
