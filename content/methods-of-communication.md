# Methods of Communication

![](https://github.com/donnemartin/system-design-primer/raw/master/images/5KeocQs.jpg)

## [[hypertext-transfer-protocol]].

- method for transporting data between client and server.
- request/response protocol.
- can be called many times with different outcomes.
- application layer protocol that relies on [[transmission-control-protocol]] and [[user-datagram-protocol]].

## [[transmission-control-protocol]].

![](https://github.com/donnemartin/system-design-primer/raw/master/images/JdAsdvG.jpg)
	- connection-oriented protocol.
		- connection is established and terminated using a handshake.
		- all packets that are sent are guaranteed to reach the destination in order.
	- good for reliability, but not the most time-efficient.
		- good for database info, ssh, ftp, etc.
		- use over [[user-datagram-protocol]] when you need all of the data to arrive intact.

## [[user-datagram-protocol]].

![](https://github.com/donnemartin/system-design-primer/raw/master/images/yzDrJtA.jpg)
- connectionless protocol.
	- data packets, called “datagrams”, are sent out and broadcast to all devices in the subnet.
	- no guarantee that packets arrive or arrive in order.
- less reliable but has much lower latency.
- useful for video calls/chat, video games, streaming, etc.

## [[remote-procedure-call]].

![](https://github.com/donnemartin/system-design-primer/raw/master/images/iF4Mkb5.png)
- a client causes a procedure to be run on a different address space *(on a remote server).*
	- there is a client stub procedure that is pushed onto a stack, and the communication module sends it to the server.
- often used for internal communications between services, hand-crafted native calls can oftentimes better fit your use case.
- public facing APIs use [[representational-state-transfer]] instead.

## [[representational-state-transfer]].

- uses GET, POST, PUT, DELETE, and PATCH requests.
- client/server model where the client acts on resources that are managed by the server.
- actions must be stateless and cacheable.
- focused on exposing data.
- great for [[horizontal-scaling]] because it is stateless.
- disadvantages.
	- some actions might not fit in the set of REST verbs.
	- complicated/nested data might require multiple round trips.
	- API responses can become bloated as new fields are added to calls that old client calls don’t need.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## References.

Categories:: [[networking]]
