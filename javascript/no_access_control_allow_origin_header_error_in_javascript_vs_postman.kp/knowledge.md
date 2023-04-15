---
title: What could be the reason that my JavaScript code is getting an error saying 'no access-control-allow-origin header is present on the requested resource', while postman does not have this issue?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The browser is blocking the request due to the same-origin policy, while Postman is not subject to this policy.
---

**Contents**

[TOC]

### Introduction

When making HTTP requests from a JavaScript code, the browser may return an error message "No Access-Control-Allow-Origin header is present on the requested resource." This error occurs due to the same-origin policy, which is a security measure that restricts the ability of a web page to access resources from another domain.

### What is the Same-Origin Policy?

The same-origin policy is a security measure that restricts the ability of a web page to access resources from another domain. It is designed to prevent malicious scripts from being able to access sensitive data from other domains. This policy is enforced by the browser, which will block requests that violate the policy.

### Why Does Postman Not Receive the Error? 

Postman is a tool used to make HTTP requests and is not subject to the same-origin policy. This means that it can make requests to any domain without being blocked by the browser.

### Conclusion 

In conclusion, the error "No Access-Control-Allow-Origin header is present on the requested resource" occurs due to the same-origin policy, which is a security measure that restricts the ability of a web page to access resources from another domain. Postman, however, is not subject to this policy, which is why it does not receive the error.
