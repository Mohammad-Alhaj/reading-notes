# Socket.io

### What are WebSocket ?

As per the conventional definition, WebSocket is a duplex protocol used mainly in the client-server communication channel. It’s bidirectional in nature which means communication happens to and fro between client-server. 


### What does the event handler io.on() do

 ---

### What Socket.IO

Socket.IO is a library that enables real-time, bidirectional and event-based communication between the browser and the server. It consists of:

a Node.js server: Source | API
a Javascript client library for the browser (which can be also run from Node.js): Source | API


### Socket.io vs Web Sockets

#### WebSocket

* It is the protocol that is established over the TCP connection

* It provides full-duplex communication on TCP connections.

* Proxy and load balancer is not supported in WebSocket.

* 	It doesn’t support broadcasting.

* It doesn’t have a fallback option.	

#### Socket

* t is the library to work with WebSocket

* Provides the event-based communication between browser and server.

* A connection can be established in the presence of proxies and load balancers.

* It supports broadcasting.

* It supports fallback options.


### When to use sockets

When you built real time applications, like Group chat Room, video conferencing, multiplayer games etc.
If you want server to push data by itself without calling from client.