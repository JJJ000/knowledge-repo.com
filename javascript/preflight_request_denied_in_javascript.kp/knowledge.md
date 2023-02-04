---
title: The preflight request was not approved by the access control check
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The server needs to respond with appropriate CORS headers to allow the request.
---

**Contents**

[TOC]

## Introduction
When making a cross-origin request from a browser, the browser will first send an HTTP request called a preflight request. The response to this preflight request must pass an access control check in order for the actual request to be allowed. If the response does not pass the access control check, the actual request will be blocked and an error will be thrown.

## Causes
The most common cause of a preflight request not passing an access control check is when the server is not configured to allow the origin making the request. This could be due to the server not having the correct CORS (Cross-Origin Resource Sharing) headers set, or it could be due to the server not being configured to allow requests from the specific origin.

## Solutions
The first step in solving this issue is to ensure that the server is correctly configured to allow requests from the origin making the request. This can be done by setting the appropriate CORS headers on the server, or by configuring the server to allow requests from the specific origin.

The second step is to ensure that the browser is sending the correct preflight request. This can be done by examining the request headers and making sure that they match the expected values.

## Conclusion
When a preflight request does not pass an access control check, it can be difficult to determine the cause. However, by ensuring that the server is configured correctly and that the preflight request is being sent with the correct headers, it is possible to resolve the issue and allow the actual request to be made.
