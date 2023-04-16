---
title: Jquery ajax requests across different domains
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery AJAX can be used to make cross domain requests in Javascript by setting the dataType option to `jsonp`.
---

**Contents**

[TOC]

1. What is Cross-Domain AJAX?
Cross-domain AJAX is a technique used to make AJAX requests to a different domain than the one the request originated from. This can be used to access data from other websites, services, and APIs.

2. How to Implement Cross-Domain AJAX?
There are a few different ways to implement cross-domain AJAX:

a. JSONP
JSONP (JSON with Padding) is a technique used to make cross-domain AJAX requests by adding a <script> tag to the page that loads a remote JavaScript file. The remote file can then execute a callback function with the data that is returned.

b. CORS
CORS (Cross-Origin Resource Sharing) is a technique used to make cross-domain AJAX requests by adding special HTTP headers to the request. This allows the server to specify which domains are allowed to make AJAX requests.

c. Proxies
Proxies are a technique used to make cross-domain AJAX requests by routing the request through a proxy server. The proxy server can then make the request to the remote server and return the response to the original requestor.

3. Benefits and Drawbacks
The main benefit of using cross-domain AJAX is that it allows data to be accessed from other websites, services, and APIs. This can be used to create dynamic and interactive web applications. The main drawback is that it can be difficult to implement and can be vulnerable to security issues.

4. Conclusion
Cross-domain AJAX is a powerful technique that can be used to access data from other websites, services, and APIs. It can be implemented using JSONP, CORS, or proxies. While it has many benefits, it can be difficult to implement and can be vulnerable to security issues.
