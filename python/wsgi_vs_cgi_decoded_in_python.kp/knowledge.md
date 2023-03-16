---
title: Can you explain wsgi and cgi in simple language?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: WSGI (Web Server Gateway Interface) and CGI (Common Gateway Interface) are two different methods for Python to communicate with web servers, with WSGI being generally preferred due to its better performance and increased flexibility.
---

**Contents**

[TOC]

# WSGI in Python
WSGI stands for Web Server Gateway Interface, and it is a specification for how web servers and Python web frameworks can communicate with each other. In simpler terms, WSGI is the interface that allows Python applications to interact with web servers. 

## How it works
When a web server receives an HTTP request, it sends the request to a WSGI server, which is a Python application that handles requests from the web server. The WSGI server then sends the request to the Python web framework, which processes the request and generates a response. The response is then sent back to the WSGI server, which sends it back to the web server to be returned to the client.

## Advantages of WSGI
One advantage of using WSGI is that it allows developers to write web applications using any Python web framework, as long as the framework is compatible with the WSGI specification. This means that developers can choose the framework that best fits their needs and still be able to deploy their application on any web server that supports WSGI.

# CGI in Python
CGI stands for Common Gateway Interface, and it is a protocol that defines how web servers can execute external programs, such as Python scripts, to generate dynamic content. In simpler terms, CGI is a way for a web server to run a Python script and use its output to generate a response to an HTTP request.

## How it works
When a web server receives an HTTP request for a CGI script, it launches the script as a separate process and passes the request data to it via environment variables and standard input. The script then generates output, which is sent back to the web server via standard output. The web server then sends the output as an HTTP response to the client.

## Advantages of CGI
One advantage of using CGI is that it is a simple and widely-supported protocol that can be used with any web server that supports it. Additionally, CGI scripts can be written in any programming language, as long as they can read input from environment variables and standard input and write output to standard output. However, CGI has some performance limitations compared to other protocols, such as FastCGI and WSGI, because it launches a separate process for each request.
