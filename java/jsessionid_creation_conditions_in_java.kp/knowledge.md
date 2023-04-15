---
title: When is a jsessionid created?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A JSESSIONID is created when a new session is created in Java.
---

**Contents**

[TOC]

1. **When a User Connects to a Web Server**
When a user connects to a web server for the first time, a JSESSIONID is created and sent back to the user as a cookie.

2. **When a User Makes a Request**
When a user makes a request to a web server, the web server checks to see if a JSESSIONID cookie exists. If a cookie does not exist, a new JSESSIONID is created and sent back to the user as a cookie.

3. **When a User Logs Out**
When a user logs out, the JSESSIONID cookie is destroyed and a new JSESSIONID is created when the user logs in again.

4. **When a Session Times Out**
When a session times out, the JSESSIONID cookie is destroyed and a new JSESSIONID is created when the user makes a new request.
