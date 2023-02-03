---
title: What is the best way to perform an ajax request without using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can make an AJAX call without jQuery in Javascript by using the XMLHttpRequest object.
---

**Contents**

[TOC]

### XMLHttpRequest

The most common way to make an AJAX call without jQuery is to use the XMLHttpRequest object. This is a built-in object in the browser that allows you to make asynchronous HTTP requests to a server.

### Creating an XMLHttpRequest Object

To create an XMLHttpRequest object, use the following code:

```
var xhr = new XMLHttpRequest();
```

### Opening a Request

Once the object is created, you need to open a request to the server. This is done with the open() method. The open() method takes three arguments: the HTTP method, the URL, and a Boolean value for whether the request is asynchronous or not.

```
xhr.open('GET', url, true);
```

### Sending the Request

Once the request is opened, you can send the request using the send() method. This method takes an optional argument which is the data that you want to send with the request.

```
xhr.send();
```
