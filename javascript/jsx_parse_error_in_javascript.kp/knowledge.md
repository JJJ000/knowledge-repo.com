---
title: Jsx elements that are next to each other must be enclosed within a single tag
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: JSX elements must be wrapped in a single parent element to prevent a parse error.
---

**Contents**

[TOC]

### What is a Parse Error?
A parse error occurs when the code you are trying to execute does not conform to the syntax rules of the language you are using. In other words, the code may contain a syntax error that prevents the code from being executed.

### What is Adjacent JSX Elements?
JSX (JavaScript XML) is an extension to the JavaScript language that allows developers to write HTML and XML-like syntax directly in their JavaScript code. Adjacent JSX elements are two or more JSX elements that are placed immediately next to each other without any other elements in between.

### What is the Solution?
The solution to this parse error is to wrap the adjacent JSX elements in an enclosing tag. This enclosing tag can be a <div> tag or any other HTML element, depending on the needs of the application. Wrapping the elements in an enclosing tag will ensure that the code is valid and can be executed without encountering any parse errors.
