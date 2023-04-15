---
title: What are the key concepts involved in the functioning of servlets? these include instantiation, sessions, shared variables, and multithreading
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Servlets work by instantiating a single instance of the servlet class, managing sessions and shared variables, and allowing for multithreading within Java.
---

**Contents**

[TOC]

### Instantiation
When a servlet is first loaded, the servlet container instantiates the servlet. The servlet container is responsible for loading the servlet class and creating an instance. The servlet container will pass any initialization parameters to the servlet's init() method.

### Sessions
Servlets can use sessions to keep track of user requests across multiple requests. A session is identified by a unique session ID and is used to store session-specific data, such as user preferences and shopping cart contents.

### Shared Variables
Servlets can use shared variables to store data that can be shared across multiple requests. This can be used to store global information, such as a database connection or configuration settings.

### Multithreading
Servlets are designed to be thread-safe, meaning that multiple requests can be handled concurrently by a single servlet instance. The servlet container will create a separate thread for each request, allowing the servlet to handle multiple requests simultaneously.
