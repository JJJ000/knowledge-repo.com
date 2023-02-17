---
title: Angular $http is sending a preflight request with the options method instead of the put/post method
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: This is due to the browser`s preflight request for cross-origin resource sharing (CORS).
---

**Contents**

[TOC]

# Introduction
Angular $http is a built-in service that provides a way for Angular applications to interact with backend services over the HTTP protocol. It is commonly used to make AJAX calls to web APIs and other web services. In some cases, when making a request using the $http service, Angular may send an OPTIONS request instead of a PUT or POST request. This can be confusing and lead to unexpected results. 

# What is an OPTIONS Request?
An OPTIONS request is an HTTP method that is used to retrieve information about the communication options available for a given URL. It is primarily used to check if a server is capable of handling a request before actually sending it. It is also used to determine if the server supports the requested HTTP method (e.g. GET, POST, PUT, etc.).

# Why is Angular Sending an OPTIONS Request?
When Angular sends an OPTIONS request, it is usually because the server does not support the requested HTTP method. This is because some servers do not support certain methods, such as PUT or POST. When Angular detects that the server does not support the requested method, it will send an OPTIONS request to check if the server supports the requested method.

# How to Avoid Sending an OPTIONS Request
If you want to avoid sending an OPTIONS request, you can do so by ensuring that the server supports the requested HTTP method. This can be done by configuring the server to support the requested method. Alternatively, you can also use a different HTTP method that is supported by the server.
