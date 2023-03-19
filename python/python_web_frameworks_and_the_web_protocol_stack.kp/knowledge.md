---
title: The integration of Python web frameworks, wsgi and cgi explained
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: WSGI is an interface for Python web frameworks to communicate with web servers, while CGI is a deprecated interface for communicating with web servers, both of which are utilized by Python web frameworks to handle requests and generate responses for web applications.
---

**Contents**

[TOC]

## Python Web Frameworks

Python is a versatile programming language for web development. Python web frameworks are libraries that provide developers with essential tools for web development, such as handling HTTP requests, database integration, and templating systems. A few popular Python web frameworks include Flask, Django, Pyramid, and CherryPy.

## WSGI

Web Server Gateway Interface (WSGI) is a specification for a universal interface between web servers and Python web applications or frameworks. WSGI specifies how web servers should communicate with Python applications, allowing for a seamless integration of Python applications with various web servers. WSGI promotes a more efficient and standardized communication between web servers and Python web applications and provides a level of interoperability among Python web frameworks.

## CGI

Common Gateway Interface (CGI) is a way for web servers to execute scripts and programs externally, such as Python scripts. CGI scripts receive requests from web browsers and return responses to web servers. CGI scripts were introduced in the early days of the World Wide Web and are still available on modern web servers.

## How They Fit Together

Python web frameworks, WSGI, and CGI are interconnected in the process of handling HTTP requests and responses. When a web browser sends a request to a web server, the web server uses WSGI to pass the request to a Python web application or framework. The Python web application handles the request and generates a response, which is passed back to the web server via WSGI. The web server then sends the response back to the web browser.

CGI scripts can also be used to handle HTTP requests and responses. In this case, when a web browser sends a request to a web server, the web server executes the CGI script, which generates a response. The web server then sends the response back to the web browser. However, WSGI has largely replaced the use of CGI scripts due to its improved efficiency and standardization. 

In summary, WSGI provides a standardized interface between web servers and Python web applications, including frameworks, while CGI is an outdated method of executing scripts externally on web servers. Python web frameworks utilize WSGI to handle HTTP requests and responses efficiently and provide a modern alternative to traditional CGI scripts.
