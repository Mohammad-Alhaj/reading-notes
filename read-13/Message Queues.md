# Message Queues

A message queue is a form of asynchronous service-to-service communication used in serverless and microservice architectures. Messages are stored on the queue until they are processed and deleted. Each message is processed only once, by a single consumer.

## Rooms

A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

You can call join to subscribe the socket to a given channel:


```
io.on("connection", (socket) => {
  socket.join("some room");
});
```

And then simply use to or in (they are the same) when broadcasting or emitting:

```
io.to("some room").emit("some event");
```


## Namespaces

A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection 


### Main namespace
```
io.on("connection", (socket) => {});
io.use((socket, next) => { next() });
io.emit("hello");
// are actually equivalent to
io.of("/").on("connection", (socket) => {});
io.of("/").use((socket, next) => { next() });
io.of("/").emit("hello");
```


### Dynamic namespaces

```
io.of((name, auth, next) => {
  next(null, true); // or false, when the creation is denied
});
```

