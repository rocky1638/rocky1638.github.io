---
type: moc
aliases: []
title: "system design moc"
date: 2022-11-26
updated: 2024-03-12
---

## book and course notes

- [[designing-data-intensive-applications]] - A very comprehensive and in-depth look at all aspects of creating a large-scale distributed system.
- [[system-design-primer]] - A higher-level overview of system design concepts from a Github guide.
- [[system-design-interview-an-insiders-guide-by-alex-yu]] - A lightweight overview of system design concepts, more focused on practical interview topics.
- [[cs75-scalability-lecture]] - An intro lecture to scalability.

## interviews

![Steps to take during a system design interview](https://github.com/ashishps1/awesome-system-design-resources/raw/main/diagrams/interview-template.png)

1. Ask initial questions to get a gauge of scale, usage, etc.
2. List out some functional requirements to get buy-in from interviewer.
3. List out some high-level non-functional requirements *(availability, r/w priority).*
4. Do back-of-envelope estimations when they’re necessary to inform a decision.
5. Think about high-level API requirements to guide your thoughts.
	- What HTTP requests will a user realistically need to hit?
6. Think about a couple database tables that are relevant to the solution.
7. Sketch out a high-level system design, that can cover the main non-functional components, making sure to justify decisions and only add details when necessary!
8. Dive into one or two key components/specifics that you feel more comfortable with.
9. Address fault-tolerance and scalability at the end.

**Meta tips:**

- Start with a naive solution, then go through functional, non-functional requirements to find where the solution breaks down.
	- Iterate over your system design diagram!
	- Only add/change things when it’s necessary!
- Tips for defining non-functional requirements.
	- Think about scalability, availability/consistency, and performance, and maybe durability if data persistence is required.
- Treat interviewer as a coworker with which you are working with.
	- Provide maximum number of positive data points!
- Call it out when you unsure about something!
- Use function call syntax (`myFunction(params)`) for API level design instead of HTTP requests.

See [[system-design-interview-questions]] for my journey in practicing these questions and giving myself feedback.
