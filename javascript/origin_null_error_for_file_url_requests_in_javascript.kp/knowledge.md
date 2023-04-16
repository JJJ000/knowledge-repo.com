---
title: The access-control-allow-origin setting does not allow requests from applications running from a file// url
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The solution is to run the application from a server instead of a file// URL.
---

**Contents**

[TOC]

# Introduction
When making a request from an application running from a file:// URL in Javascript, the error “Origin null is not allowed by Access-Control-Allow-Origin” may be encountered. This error is caused by the same-origin policy, which restricts the ability of a web page to make requests to a different domain. In this article, we will discuss the causes of this error and how to address it.

# Causes
The “Origin null is not allowed by Access-Control-Allow-Origin” error is caused by the same-origin policy, which restricts the ability of a web page to make requests to a different domain. When a request is made from a file:// URL, the browser will set the Origin header to null, which is not allowed by the server.

# Solutions
There are several solutions to this issue. The first is to use a proxy server to make the request. This will allow the request to be made from the same domain as the application, thus bypassing the same-origin policy. Another option is to enable CORS (Cross-Origin Resource Sharing) on the server. This will allow the request to be made from a different domain. Finally, the server can be configured to allow requests from all origins by setting the Access-Control-Allow-Origin header to “*”.

# Conclusion
The “Origin null is not allowed by Access-Control-Allow-Origin” error can be encountered when making a request from an application running from a file:// URL in Javascript. This error is caused by the same-origin policy, which restricts the ability of a web page to make requests to a different domain. There are several solutions to this issue, including using a proxy server, enabling CORS, and setting the Access-Control-Allow-Origin header to “*”.
