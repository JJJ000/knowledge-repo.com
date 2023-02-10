---
title: Are modern browsers still vulnerable to JSON hijacking?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, JSON Hijacking is still an issue in modern browsers and can be prevented by using methods such as using HTTPS and using proper authorization.
---

**Contents**

[TOC]

### What is JSON Hijacking?
JSON Hijacking is a technique used to exploit the use of the JavaScript Object Notation (JSON) format to gain unauthorized access to data. It is a type of Cross-Site Request Forgery (CSRF) attack, but uses JSON instead of HTML.

### How Does JSON Hijacking Work?
JSON Hijacking works by exploiting the fact that JSON data can be loaded in the browser using a <script> tag. An attacker can create a malicious script that will make a request to a vulnerable server and return the data as JSON. The attacker can then access the data by accessing the JavaScript object that was returned.

### Is JSON Hijacking Still an Issue?
Fortunately, modern browsers have taken steps to mitigate the risk of JSON Hijacking. The same-origin policy has been implemented in all major browsers, which prevents malicious scripts from being able to make requests to other domains. Additionally, the Content Security Policy (CSP) can be used to further restrict the ability of malicious scripts to access data from other domains. As such, JSON Hijacking is not as much of an issue as it once was.
