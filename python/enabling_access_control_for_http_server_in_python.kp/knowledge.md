---
title: Implement access control on a basic http server
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: One possible answer could be `You can enable access control on a simple HTTP server in Python by implementing authentication and authorization mechanisms, such as using a username and password or checking the user`s IP address.`
---

**Contents**

[TOC]

## Introduction

HTTP servers are software applications that handle requests and responses over the HTTP protocol. Access control is a security feature that restricts access to resources based on pre-defined rules. In this article, we'll explore how to enable access control on a simple HTTP server in Python.

## Creating a Simple HTTP server

Before we can enable access control, we need to create a simple HTTP server in Python. Here's an example:

```python
import http.server
import socketserver

PORT = 8000

Handler = http.server.SimpleHTTPRequestHandler

with socketserver.TCPServer(("", PORT), Handler) as httpd:
    print("serving at port", PORT)
    httpd.serve_forever()
```

This creates an HTTP server on port 8000 that serves files from the current directory.

## Enabling Basic Access Control

One way to enable access control is to use Basic Authentication. Basic Authentication requires users to provide a username and password to access protected resources.

Here's how we can enable Basic Authentication on our HTTP server:

```python
import http.server
import socketserver
from http import HTTPStatus

PORT = 8000
USERNAME = 'admin'
PASSWORD = 'password'

class AuthHandler(http.server.SimpleHTTPRequestHandler):
    def do_HEAD(self):
        self.send_response(HTTPStatus.UNAUTHORIZED)
        self.send_header('WWW-Authenticate', 'Basic realm="Restricted Area"')
        self.end_headers()

    def do_AUTHHEAD(self):
        self.send_response(HTTPStatus.UNAUTHORIZED)
        self.send_header('WWW-Authenticate', 'Basic realm="Restricted Area"')
        self.send_header('Content-type', 'text/html')
        self.end_headers()

    def do_GET(self):
        if not self.headers.get('Authorization'):
            self.do_AUTHHEAD()
            self.wfile.write(b'no auth header received')
        elif self.headers.get('Authorization') == 'Basic '+str(base64.b64encode(bytes(f"{USERNAME}:{PASSWORD}", "utf-8")), "utf-8"):
            http.server.SimpleHTTPRequestHandler.do_GET(self)
        else:
            self.do_AUTHHEAD()
            self.wfile.write(b'not authenticated')

Handler = AuthHandler

with socketserver.TCPServer(("", PORT), Handler) as httpd:
    print("serving at port", PORT)
    httpd.serve_forever()
```

In this code, we created a new class, `AuthHandler`, that inherits from `SimpleHTTPRequestHandler`. The `AuthHandler` class overrides the `do_HEAD` and `do_GET` methods to implement Basic Authentication.

The `do_HEAD` method sends an unauthorized response with a header that tells the client to use Basic Authentication. The `do_GET` method checks if the client has provided the correct username and password in the Authorization header. If the client is not authenticated, the `do_AUTHHEAD` method is called to send an unauthorized response. If the client is authenticated, the `do_GET` method from the parent class (`SimpleHTTPRequestHandler`) is called to serve the requested file.

## Enabling Role-based Access Control

Basic Authentication is a simple way to restrict access to resources, but it doesn't provide fine-grained control over who can access what. Role-based access control is a more advanced form of access control that allows access based on the role of the user.

Here's how we can enable role-based access control on our HTTP server:

```python
import http.server
import socketserver
from http import HTTPStatus

PORT = 8000

AUTH_CONFIG = {
    'admin': 'password',
    'user': 'password',
}

ROLE_CONFIG = {
    '/admin': 'admin',
    '/user': 'user',
}

class RBACHandler(http.server.SimpleHTTPRequestHandler):
    def do_HEAD(self):
        self.send_response(HTTPStatus.UNAUTHORIZED)
        self.send_header('WWW-Authenticate', 'Basic realm="Restricted Area"')
        self.end_headers()

    def do_AUTHHEAD(self):
        self.send_response(HTTPStatus.UNAUTHORIZED)
        self.send_header('WWW-Authenticate', 'Basic realm="Restricted Area"')
        self.send_header('Content-type', 'text/html')
        self.end_headers()

    def get_role(self):
        for path, role in ROLE_CONFIG.items():
            if self.path.startswith(path):
                return role
        return None

    def check_auth(self):
        auth_header = self.headers.get('Authorization')
        if not auth_header:
            return False
        auth = auth_header.split(' ')[1]
        auth = base64.b64decode(auth).decode('utf-8')
        username, password = auth.split(':')
        return AUTH_CONFIG.get(username) == password

    def do_GET(self):
        role = self.get_role()
        if not role:
            http.server.SimpleHTTPRequestHandler.do_GET(self)
            return
        if not self.check_auth():
            self.do_AUTHHEAD()
            self.wfile.write(b'not authenticated')
            return
        if role != self.check_auth():
            self.do_AUTHHEAD()
            self.wfile.write(b'not authorized')
            return
        http.server.SimpleHTTPRequestHandler.do_GET(self)

Handler = RBACHandler

with socketserver.TCPServer(("", PORT), Handler) as httpd:
    print("serving at port", PORT)
    httpd.serve_forever()
```

In this code, we created a new class, `RBACHandler`, that inherits from `SimpleHTTPRequestHandler`. The `RBACHandler` class overrides the `do_GET` method to implement role-based access control.

The `get_role` method checks the `ROLE_CONFIG` dictionary to find the role associated with the requested resource. The `check_auth` method checks the username and password provided in the Authorization header against the `AUTH_CONFIG` dictionary.

If the requested resource is not protected, the method from the parent class is called. Otherwise, if the client is not authenticated or authorized, an unauthorized response is sent. Finally, if the client is authenticated and authorized, the method from the parent class is called to serve the requested file.

## Conclusion

In this article, we explored how to enable access control on a simple HTTP server in Python. We discussed two ways to implement access control: Basic Authentication and Role-based Access Control. These security features can help protect web resources from unauthorized access.
