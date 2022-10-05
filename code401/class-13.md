# Class 13 - Message Queues

## [Socket.io Chat Example](https://socket.io/get-started/chat/)

### What proof of life are we getting on the backend from the above app?

Whenever a user connects, a console log is sent to the back-end portion that reads "a user connected." When a user leaves the chat, a similar message is logged, reading "a user disconnected."

### Socket.IO gives us the io.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?
The `.broadcast` flag allows us to specify that the message should be emitted to all connected sockets _except_ for the socket it was sent from. Typically, if a socket is listening for a message and emits that same message, it will also receive that message.

## [Rooms](https://socket.io/docs/v4/rooms)

### What is a room and how might a room be useful?

In Socket.IO, rooms are a server-side concept that allow for sockets to join different "channels". It allows the server to send messages only to a subset of clients.

### How do you join a room?

The server specifies the socket and calls `.join('roomname')`. From there, the server can specify `.to('roomname')` before each `.emit()` method to say that the emission should only go to a certain room.

### how do you leave a room?

`.leave(roomname)` is called in the same manner as `.join()` to leave a room

## [Namespaces](https://socket.io/docs/v4/namespaces/)

### What is a Namespace and what does it allow you to do?

A namespace allows us to communicate over what _looks_ like different channels, but is in reality a single channel. The server is able to route messages to the correct namespace.

### Each namespace potentially has its own what? (hint: 3 things)

Event handlers, middleware, and rooms

### Discuss a possible use case for separate namespaces

A use case for namespaces would be a multi-tenant application. We may have an application where a user may have a certain responsibility (Say, a driver, a vendor, and a customer). We can have these tenants communicate using the same server, but we can separate them into separate namespaces to section out their logic.