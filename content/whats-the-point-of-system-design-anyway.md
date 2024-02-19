---
created_at: 2024-01-26
type: writing
aliases: 
parents:
  - "[[designing-data-intensive-applications|ddia]]"
---

# What’s the point of system design anyway?

The question we want to answer:

Why does so much change when we go from showing our friends our cool side project to wanting to serve millions (or even billions) of users?

# The holy trinity

Just like a classic French chicken stock needs the holy _mirepoix_ trinity of carrot, celery, and onion, our systems need a trio of **non-functional properties** in order to keep users (and developers) happy.

## Reliability

> [!info] Definition
> A system is **reliable** if it works under adversity.

[[reliability|Reliability]] is a measure of how confident a user can be that when they want to do something with our system, our system will be there to _do that thing._

Although this might sound simple at first, there are many things that can go wrong with a system, called **faults**, especially when there are a lot of machines running your code, and many people trying to communicate with those machines.

The first class of these faults is **hardware faults**, including but not limited to:

- Your server’s hard drive crashes.
- The power goes out in your data center.
- Your data center admin trips and accidentally unplugs some wires.

In the past, redundant hardware components were enough to mitigate these issues, but as computing demands increase and the number of machines being used at once increases, there has been a trend of just _creating systems that can tolerate the loss of entire machines._ This will be a primary focus as we get into more specific system design topics.

The second class of fault is **software faults.** Unlike hardware faults, these errors are typically systematic rather than random, making them more prone to causing major outages, as everything is more likely to fail instead of just one random component. Once again, some examples include:

- A function that doesn’t account for a specific class of input, crashing whenever it receives it.
- A runaway process/infinite loop.
- Forgetting to handle subtle edge cases (time-zones, off-by-one errors, etc).

So with all of this in mind, how do we design systems that are both reliable and **fault-tolerant?**

Meaningful test coverage, well-abstracted code, and efficient roll-back scripts are some industry best-practices that instill trust in system [[availability]] and resilience. By working from these fundamentals, we ensure our systems avoid **failures** even when facing **faults.**

## Scalability

A system is **scalable** if it can adequately handle increases in workload and demand.

When describing [[scalability]], it’s important to first understand how to describe load. There are several concepts that can help us here:

- **Throughput:** This is a measure of how much data or how many records a system can process in a period of time (usually a second). This is usually more valued in batch processing systems, like encoding/compressing videos uploaded to YouTube, or generating aggregated invoices for all shop owners on Shopify.

> [!info] Not all throughput is built the same
> Systems will need to adapt differently to different throughput. A system that handles 2M requests of 1KB each per second versus one that handles 100 requests of 2GB per second need to be designed differently.

- **Response Time:** This, like it sounds, is how fast it takes for any single request to be resolved by the system. This is much more valuable in **online systems**, where any slowdown can lead to dissatisfaction with the end user, or compounding slowdown in the rest of your system.

> [!important] Percentiles!
> When measuring response times, consider **percentiles**, and not just **average** response times.
>
> e.g. if your system responds in 200ms for 80% of requests, but takes 20s to respond to the other 20%, then your users are very unhappy 20% of the time, even if the average response time is still reasonable.

This is especially relevant in systems where multiple requests are necessary to fulfill a user’s request. If we have to wait for all the requests to complete, then the fact that most of the responses completed quickly is irrelevant. Just think back to the time when you went out to a restaurant when everyone was waiting to eat with their food in front of them while your friend Kevin was sitting there with an empty table in front of him because his order got forgotten by the kitchen.

## Maintainability

> [!info] Definition
> A system is **maintainable** when many people can work productively on the system.

Kleppman suggests that there are three main pillars of making a maintainable system.

1. **Operability:** An operation team (on-call engineers, support engineers, IT) should be able to easily and routinely check the performance of systems through [[observability]], do maintenance, have good alerting and documentation, etc.
2. **Simplicity:** Good abstractions should be able to make complex projects more manageable and wrap-your-head-around-able, leading to fewer bugs and code that’s easier to update.
3. **Evolvability:** As well as adding simplicity, good abstractions also make it easier to make changes to code as needs change. For example, code that has business logic decoupled with library-specific logic will be easier to update if you need the library to be changed.
