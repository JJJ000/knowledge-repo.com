---
title: Can you explain why flask utilizes context stacks?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Flask`s context stacks provide a way to manage active contexts and their associated resources within the application`s execution environment.
---

**Contents**

[TOC]

### Introduction
Flask is a popular web framework written in Python that is designed for building web applications. Flask provides a mechanism for storing information that is available for the duration of a single request/response cycle. This mechanism is known as a context stack.

### What is a context stack?
A context stack is a way of keeping track of information that is relevant to the execution of a particular piece of code. In Flask, there are two primary context stacks that are used: the application context stack and the request context stack.

### Application context stack
The application context stack is used to store information that is relevant to the entire application. This includes items like the configuration for the application, registered extensions, and database connections. The application context stack is created when the Flask application is instantiated and is torn down when the application is shut down.

### Request context stack
The request context stack is used to store information that is relevant to a single request/response cycle. This includes items like the request object, the current user, and any database connections that are needed for the request. The request context stack is created at the beginning of a request and is torn down when the request has been completed.

### Conclusion
The use of context stacks in Flask makes it easy to store and access information that is relevant to a specific piece of code, whether it is the entire application or a single request. By using context stacks, Flask is able to provide a clean and well-organized framework for building web applications.
