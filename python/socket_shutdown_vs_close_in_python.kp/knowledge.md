---
title: What is the difference between 'socket.shutdown' and 'socket.close'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: `socket.shutdown` only terminates the connection while `socket.close` closes the connection and frees up resources used by the socket object.
---

**Contents**

[TOC]

Socket Shutdown vs Socket Close in Python

When you're working with networking applications in Python, you use the `socket` module to create sockets that can send and receive data. However, when you're done with a socket, you can't simply stop using it. You need to explicitly close it, or it might prevent your program from ending properly. But what's the difference between shutting down a socket and closing it? 

### What is Socket Shutdown?

`shutdown()` is a built-in method in the `socket` module that allows you to stop one or both ends of a connection from sending or receiving data. This means that you can use `shutdown()` to close just one direction of the connection, or both.

```python
import socket

# create a socket object
server_socket = socket.socket()

# bind the socket to a public host, and a port
server_socket.bind(('localhost', 9999))

# listen for incoming connections
server_socket.listen()

# accept connections from outside
(client_socket, address) = server_socket.accept()

# send and receive data
# ...

# close the input and output channels
client_socket.shutdown(socket.SHUT_RDWR)
```

In this example, we've created a server that listens for incoming connections. When a client connects, we accept the connection and create a `client_socket` object that we can use to send and receive data. 

After we're done sending and receiving data, we call `client_socket.shutdown(socket.SHUT_RDWR)` to tell the client that we're done sending data, and that it should close its end of the connection. 

### What is Socket Close?

`close()` is a built-in method in the `socket` module that allows you to close a socket when you're done using it. Once you've called `close()`, the socket is no longer usable, and any attempts to use it will result in an error.

```python
import socket

# create a socket object
client_socket = socket.socket()

# connect the client to a remote host and port
client_socket.connect(('localhost', 9999))

# send and receive data
# ...

# close the socket
client_socket.close()
```

In this example, we create a client that connects to a server on the same machine, on port 9999. Once we're done sending and receiving data, we call `client_socket.close()` to close the socket. 

### When Should You Use Shutdown vs Close?

The `shutdown()` method is useful when you want to close just one direction of a connection, or when you want to send a signal to the other end of the connection that you're done sending data. 

The `close()` method is useful when you're completely done with the socket, and you want to free up any resources it's using. 

In most cases, you'll want to call both `shutdown()` and `close()`. Call `shutdown()` first to tell the other end of the connection that you're done sending data, then call `close()` to release any resources that the socket is using. 

### Conclusion

Now you know the difference between `shutdown()` and `close()` in Python's `socket` module. If you're done with a socket, don't forget to close it or you might leave your program in a strange state!
