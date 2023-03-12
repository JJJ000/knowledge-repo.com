---
title: What is the way to check for an available and active network connection using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `socket` module and try to create a connection to a remote host.
---

**Contents**

[TOC]

## Checking for Network Connection in Python

When developing network applications, it's important to ensure that there's an available and active network connection before sending or receiving data. In Python, there are several ways to check for network connection. 

### Method 1: Ping a Remote Server

One way to check for network connection in Python is to ping a remote server. The idea behind this is simple: if the server is reachable, then there's an active network connection. Here's how to do it:

```python
import subprocess

def check_connection():
    try:
        # Ping Google's DNS server
        process = subprocess.Popen(['ping', '-c', '1', '8.8.8.8'], stdout=subprocess.PIPE)
        output = process.communicate()[0]
        
        # Check if the message "1 received" exists in the output
        if b'1 received' in output:
            return True
        else:
            return False
    except:
        return False
```

In this example, we use the `subprocess` module to run the ping command. We ping Google's DNS server and check if we receive a response. If we do, then there's an active network connection.

### Method 2: Use the `socket` Module

Another way to check for network connection in Python is to use the `socket` module. Here's how to do it:

```python
import socket

def check_connection():
    try:
        # Create a socket object
        socket.create_connection(('www.google.com', 80))
        return True
    except OSError:
        return False
```

In this example, we create a socket object and try to connect to Google's website on port 80. If we're able to connect, then there's an active network connection. If not, then there's no network connection.

### Method 3: Use the `requests` Module

Finally, we can also check for network connection using the `requests` module, which is a popular library for sending HTTP requests in Python. Here's how to do it:

```python
import requests

def check_connection():
    try:
        # Send a GET request to Google's homepage
        response = requests.get('http://www.google.com')
        if response.status_code == 200:
            return True
        else:
            return False
    except:
        return False
```

In this example, we send a GET request to Google's homepage and check if we receive a successful response (status code 200). If we do, then there's an active network connection. If not, then there's no network connection.
