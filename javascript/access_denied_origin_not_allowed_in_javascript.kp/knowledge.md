---
title: Access-control-allow-origin does not permit origin
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, it is not allowed.
---

**Contents**

[TOC]

# Access-Control-Allow-Origin
Access-Control-Allow-Origin (ACAO) is an HTTP header that determines whether a browser can access a resource from a different origin (domain, protocol, or port). 

# How Does it Work?
When a browser makes a cross-origin request, it sends an Origin header with the request. The server then checks the Access-Control-Allow-Origin header to see if the origin is allowed to access the resource. If it is, the browser will allow the request to proceed. If not, the browser will block the request.

# Implications
This means that if the Access-Control-Allow-Origin header is not set correctly, then the browser will not allow the request to proceed and the resource will not be loaded. This can lead to errors and can prevent the intended functionality of the page.

# Conclusion
In summary, Access-Control-Allow-Origin is an important HTTP header that determines whether a browser can access a resource from a different origin. If it is not set correctly, the browser will block the request and the resource will not be loaded.
