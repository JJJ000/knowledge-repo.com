---
title: Why do people insert code such as "throw 1; <dont be evil>" and "for(;;);" before JSON responses?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: These codes are used to prevent malicious code from being executed when the response is parsed.
---

**Contents**

[TOC]

1. What is the Purpose?
##
The purpose of adding "throw 1; <dont be evil>" and "for(;;);" to a json response is to prevent attackers from exploiting a vulnerability in web applications that use JSON.

2. What is the Vulnerability?
##
The vulnerability is known as a Cross-Site Scripting (XSS) attack. XSS attacks occur when an attacker injects malicious code into a web application, which then runs in the user's browser. This malicious code can be used to steal user data, hijack user sessions, or redirect the user to malicious websites.

3. How Does the Code Prevent XSS Attacks?
##
The code "throw 1; <dont be evil>" and "for(;;);" is used to prevent XSS attacks by preventing the malicious code from being executed. The code "throw 1; <dont be evil>" is used to stop the execution of the malicious code, while "for(;;);" is used to prevent the malicious code from being parsed by the browser.

4. What are the Limitations?
##
The code is only effective against XSS attacks and does not protect against other types of attacks. Additionally, the code may not be effective against all browsers, as some browsers may not recognize the code and allow the malicious code to be executed.
