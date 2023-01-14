---
title: What is the purpose of google adding `while(1);` to the beginning of their json responses?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-14 00:00:00
updated_at: 2023-01-14 00:00:00
tldr: Google prepends `while(1);` to their JSON responses in order to prevent malicious code execution.
---

**Contents**

[TOC]

### Overview
Google prepends `while(1);` to their JSON responses in order to prevent Cross-site Script Inclusion (XSSI) attacks. XSSI attacks are a type of security vulnerability that can be used to steal data from a website by exploiting the way that web browsers process JavaScript. By prepending `while(1);` to the JSON response, Google is able to protect the data from being accessed by malicious actors.

### What is Cross-site Script Inclusion (XSSI)?
Cross-site Script Inclusion (XSSI) is a type of security vulnerability that occurs when an attacker is able to inject malicious code into a website. This code can be used to access data stored on the website, such as user information or sensitive files. XSSI attacks are often used to steal data from websites, as it can be difficult for the website to detect and prevent the attack.

### How Does Google Protect Against XSSI?
Google prepends `while(1);` to their JSON responses in order to prevent XSSI attacks. By prepending this string to the beginning of the response, Google is able to ensure that the data is not interpreted as valid JavaScript by the web browser. This makes it difficult for attackers to access the data, as it is not possible to execute code in the response.

### Conclusion
Google prepends `while(1);` to their JSON responses in order to protect the data from XSSI attacks. By prepending this string to the response, Google is able to ensure that the data is not interpreted as valid JavaScript by the web browser, making it difficult for attackers to access the data.
