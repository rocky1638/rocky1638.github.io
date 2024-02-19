---
created_at: 2023-01-03
type: concept
aliases: []
---

# Clean Architecture

![](https://raw.githubusercontent.com/mattia-battiston/clean-architecture-example/master/docs/images/clean-architecture-diagram-2.png)

## The value it can provide.

- **Effective testing strategy** that follows the testing pyramid.
- Frameworks are isolated in individual modules so that when (not if) we change our mind we only have to change one place, with the rest of the app not even knowing about.
	- The app has **use cases rather than being tied to a CRUD system.**
- **Screaming architecture** a.k.a. it screams its intended usage.
	- When you look at the package structure you get a feel for what the application does rather than seeing technical details.
- All business logic is in a use case so it's easy to find and it's not duplicated anywhere else
- Hard to do the wrong thing because modules enforce compilation dependencies.
- It is **always ready to deploy** by leaving the wiring up of the object for last or by using feature flags, so we get all the benefits of continuous integration.
- Good monolith with clear use cases that you **can split in microservices later**, once you've learnt more about them.

## The four main components.

### Entities.

- Represent your domain object.
- Apply only logic that is applicable in general to the whole entity *(e.g. validating the format of an hostname)*.
- **Plain objects: no frameworks**, no annotations
- As close to a [[database]] model definition as possible.

### Use cases.

- Represent your business actions, it’s what you can do with the application.
	- **Expect one use case for each business action.**
- Pure business logic, plain code *(expect maybe some `utils` libraries)*, framework-agnostic.
- The **use case doesn't know who triggered it** and how the results are going to be presented *(e.g. could be on a web page, or - returned as json, or simply logged, etc.)*.
- Throws business exceptions.

### Interfaces / Adapters.

- **Retrieve and store data** from and to a number of sources *(database, network devices, file system, 3rd parties, etc.)*.
- **Implement the interfaces defined by the use case.**
- Are ways to interact with the application, and typically involve a delivery mechanism (e.g. REST APIs, scheduled jobs, GUI, other systems)
- **Trigger a use case** and convert the result to the appropriate format for the delivery mechanism.
- The controller for a MVC.
- Not framework-agnostic, specific adapters/interfaces for each framework/input/output format.

### External interfaces.

- Use whatever framework is most appropriate *(they are going to be isolated here anyway)*.
- What the client/app interacts with.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

- https://github.com/Createdd/Writing/blob/master/2018/articles/CleanA.md#the-concept---presented-in-bullet-points

Categories::
