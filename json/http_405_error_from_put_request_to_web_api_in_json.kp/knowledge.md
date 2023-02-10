---
title: A put request to a web API results in an http 405 method not allowed error
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The PUT method is not allowed for the requested resource, resulting in an HTTP 405 Method Not Allowed error.
---

**Contents**

[TOC]

## What is an Http 405 Method Not Allowed Error?
An HTTP 405 Method Not Allowed error is an HTTP response status code indicating that the request method is known by the server but is not supported by the target resource. This is most often seen when the client attempts to use a request method that is not supported by the server.

## What Causes an Http 405 Method Not Allowed Error?
The most common cause of an HTTP 405 Method Not Allowed error is when the client attempts to use a request method that is not supported by the server. This can happen when the client attempts to use a PUT or DELETE request on a resource that does not support those methods.

## How to Resolve an Http 405 Method Not Allowed Error
To resolve an HTTP 405 Method Not Allowed error, the client should ensure that the request method is supported by the server. If the request method is not supported, the client should use an alternate request method that is supported by the server. Additionally, the server should be configured to allow the request method that the client is attempting to use.
