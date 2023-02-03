---
title: A frame attempting to access a cross-origin frame was blocked due to a securityerror
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The browser prevents a frame from accessing a cross-origin frame to protect against malicious attacks.
---

**Contents**

[TOC]

# Solution

## Overview
Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources (e.g. fonts, JavaScript, etc.) on a web page to be requested from another domain outside the domain from which the resource originated. When a web page tries to access a resource from a different domain, an error is thrown: "Blocked a frame with origin from accessing a cross-origin frame." This error is thrown because the browser is trying to protect the user from potential malicious activities.

## Causes
This error is typically caused by a misconfigured CORS policy. The CORS policy defines which domains are allowed to access resources on a website. If the domain of the requesting page is not included in the CORS policy, the browser will block the request and throw the error.

## Solutions
The most common solution to this error is to add the domain of the requesting page to the CORS policy. If the domain is not known, the CORS policy can be set to allow all domains by using the wildcard character (“*”).

Another solution is to use a proxy server. A proxy server is a server that acts as an intermediary between the requesting page and the requested resource. The proxy server will make the request to the resource on behalf of the requesting page and will return the response to the requesting page. This can be used to bypass the CORS policy and allow access to the resource.
