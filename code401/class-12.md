# Class 12

## Web Sockets

### What is a Web Socket?

A Web Socket allows clients/web applications to maintain two-way communication with a server. Once a connection is established, the connected machines can communicate in real-time using Event Driven Architecture.

### Describe the Web Socket request/response handshake and what happens once the connection is established

First, a client reaches out to the server using an HTTP request. This request contains the following -

```HTTP
GET /chat HTTP/1.1
Host: server.example.com
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Key: x3JJHMbDL1EzLkh9GBhXDw==
Sec-WebSocket-Protocol: <protocol>
Sec-WebSocket-Version: 13
Origin: http://example.com
```

The server responds with an HTTP response. The response contains the following -

```http
HTTP/1.1 101 Switching Protocols
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Accept: HSmrc0sMlYUkAGmm5OPpG2HaGWk=
Sec-WebSocket-Protocol: <protocol>
```

Once this response is received, further communication can be made with the server using bi-directional protocol.

### Web Sockets provide a standardized way for the server to send content to a client without first receiving an HTTP request from that client

## Socket.IO

### What does the event handler io.on() do?

In Socket.IO, the `.on()` takes in the name of an event and a _listener_ function. `io` typically acts as the overall server instance, so this `.on()` will listen for events from all connected clients.

### Describe some possible proof of life or proof that the code works as expected

If we want to define proof of life for an event handler, we could add a simple console log to the `.on()` handler. This could be important especially if we don't necessarily need the event to change something in the user interface.

### What does socket.emit() do?

`socket.emit()` is called from a client, and is passed in an `event name` and any number of arguments. The arguments will get passed to event handlers that listen to this emit.

## Socket.io vs Web Sockets

### What is the difference between WebSocket and Socket.IO?  

> It is built on top of the WebSocket protocol and provides additional guarantees like fallback to HTTP long-polling or automatic reconnection. -- _[Socket.io Documentation](https://socket.io/docs/v4/)_

### When to use Socket.IO vs WebSockets

The use-cases for each depend on prefence and business needs. Socket.IO allows for fallback and implements some features not found in the WebSocket standard, such as rooms. Socket.IO is also thoroughly tested, so if you need the features it provides, it can be helpful.  
On the other hand, there is some overhead with Socket.IO. The fallback functionality creates extra HTTP requests, albeit pretty small ones.  
As with many things, it's a question of what's important. Do we need full control over our socket implementation? Maybe we use WebSocket, but it's going to take some time and effort to architect in a robust manner. Do we need to spin up a project quickly? Maybe we reach for Socket.IO and take advantage of its known features.