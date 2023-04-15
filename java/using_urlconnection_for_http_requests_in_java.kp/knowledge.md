---
title: How to create and handle http requests with java.net.URLConnection?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `openConnection()` method on a java.net.URL object to create a URLConnection object, then use the methods on that object to fire and handle HTTP requests.
---

**Contents**

[TOC]

### Creating an HTTP Request

Creating an HTTP request using `java.net.URLConnection` involves the following steps:

1. Create a `java.net.URL` object with the URL of the desired resource.
2. Create a `java.net.URLConnection` object by calling the `openConnection()` method on the `java.net.URL` object.
3. Set any necessary HTTP request properties by calling the `setRequestProperty()` method on the `java.net.URLConnection` object.
4. Open an output stream to the `java.net.URLConnection` object by calling the `getOutputStream()` method.
5. Write the request data to the output stream.
6. Close the output stream.

### Handling an HTTP Response

Handling an HTTP response using `java.net.URLConnection` involves the following steps:

1. Open an input stream to the `java.net.URLConnection` object by calling the `getInputStream()` method.
2. Read the response data from the input stream.
3. Close the input stream.
4. Retrieve any necessary HTTP response properties by calling the `getHeaderField()` method on the `java.net.URLConnection` object.
