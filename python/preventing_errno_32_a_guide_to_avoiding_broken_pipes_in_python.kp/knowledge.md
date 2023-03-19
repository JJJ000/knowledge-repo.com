---
title: What steps can be taken to avoid errno 32, which results in a broken pipe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Keep the reader or writer end of the socket open while the other end is still sending or receiving data.
---

**Contents**

[TOC]

## Introduction

When working on Python sockets, it's common to encounter the "broken pipe" error. This error usually happens when the client disconnects unexpectedly before the server sends a response or a large amount of data. In this guide, we'll discuss some ways to prevent the errno 32 broken pipe error in Python.

## Use Exception Handling

One way to prevent a broken pipe error is to use exception handling. When we send data to a client, it's crucial to handle any exceptions that may occur. We can use the `try-except` statement to handle the broken pipe error. Here is an example:

```
import socket

client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.connect(("localhost", 8080))

try:
    client.sendall(b"Hello World!")
except socket.error as e:
    print(f"Error: {e}")
    client.close()
```

In this code, we're handling the socket error exception by closing the client socket when it occurs.

## Set TCP Keepalive

Another way to prevent the broken pipe error is to set the TCP keepalive option. The TCP keepalive option allows the client to detect if the connection has been lost due to network issues or the remote client crashing. Here's an example of using the TCP keepalive option:

```
import socket

# Set TCP Keepalive
client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.setsockopt(socket.SOL_SOCKET, socket.SO_KEEPALIVE, 1)

# Connect to server
client.connect(("localhost", 8080))

# Send data
client.sendall(b"Hello World!")
```

By setting the TCP keepalive option, we ensure that the client detects if the connection has been lost and takes appropriate measures to prevent broken pipe errors.

## Use Non-Blocking I/O

Using non-blocking I/O can also help in preventing the broken pipe error. When using non-blocking I/O, the socket will not block if there's no data to read or send. Here's an example:

```
import socket

# Set socket to non-blocking mode
client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.setblocking(False)

# Connect to server
client.connect(("localhost", 8080))

# Send data
data = b"Hello World!"
total_sent = 0
while total_sent < len(data):
    try:
        sent = client.send(data[total_sent:])
        if sent == 0:
            raise socket.error("Broken Pipe")
        total_sent += sent
    except socket.error as e:
        print(f"Error: {e}")
        client.close()
        break
```

In this code, we're using non-blocking I/O to send data to the server. If any socket error occurs, we close the client socket.

## Conclusion

By using exception handling, setting TCP keepalive, or using non-blocking I/O, we can prevent the broken pipe error in Python. When sending data to clients, it's essential to handle any exceptions that may occur, set TCP keepalive, or use non-blocking I/O to ensure smooth communication between the client and server.
