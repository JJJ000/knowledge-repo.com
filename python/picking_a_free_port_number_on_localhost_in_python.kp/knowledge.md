---
title: How can I select an available port number when working on localhost?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use `0` as the port number argument when creating a socket in Python, and the operating system will automatically select a free port number.
---

**Contents**

[TOC]

## Checking for free ports

To pick a free port number in Python, you must first check for available ports that have not been assigned to other processes. This can be achieved by writing a function that tries to bind to ports in a sequential manner and returns the first available port.

```python
import socket


def get_free_port():
    # Create a socket object
    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    # Get the system hostname
    host = socket.gethostname()
    # Iterate over a range of port numbers
    for port in range(8000, 9000):
        try:
            # Try binding to the port
            sock.bind((host, port))
            # If successful return the port number
            return port
        except:
            # If port is in use, continue to the next one
            continue
```

This function tries to bind to a range of port numbers from 8000 to 9000. The socket object is created using socket.AF_INET to specify the address family as IPv4 and socket.SOCK_STREAM to specify the socket type as TCP. The socket is bound to the host and port in the for loop, and if successful the function returns the port number.


## Using a free port

Once you have found a free port number using the above function, you can use it to start a server or bind to a client socket.

```python
import socket


def start_server():
    # Get a free port number
    port = get_free_port()
    # Create a socket object
    server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    # Bind the socket to a specific address and port
    server_socket.bind((socket.gethostname(), port))
    # Listen for incoming connections
    server_socket.listen(5)
    # Server code...

def connect_to_server():
    # Get a free port number
    port = get_free_port()
    # Create a socket object
    client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    # Connect to the server
    client_socket.connect((socket.gethostname(), port))
    # Client code...
```

In the above example, the free port number is assigned to the server and client sockets using the `get_free_port()` function. The `server_socket` object is bound to the host and port and begins listening for incoming connections. The `client_socket` object is used to connect to the server by specifying the server's host and port.


## Caveats

It's important to note that finding a free port using the method described above is not foolproof. Another process may bind to the port number after the check, but before your process tries to bind to it. In cases where multiple processes need to bind to a particular port number, it's better to use a system that can manage port numbers, such as Docker or Kubernetes. Additionally, it's a good practice to set a timeout on your sockets, so that they do not hang indefinitely if a client does not connect or if data transfer takes too long.
