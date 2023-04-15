---
title: What is the distinction between a future and a promise?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Future represents the result of an asynchronous computation, while a Promise is an object that acts as a proxy for a result that is initially unknown.
---

**Contents**

[TOC]

### Definition
A Future is an object that acts as a reference to the result of an asynchronous operation. It is a placeholder object for an asynchronous task, allowing the task to be executed in a different thread than the one in which it was created.

A Promise is an object that acts as a proxy for a result that is initially unknown. It allows an asynchronous function to return a value at some point in the future, providing a way for the caller to register callbacks for when the value is available.

### Usage
A Future is used to represent the result of an asynchronous computation, such as a network call or a database query. It allows the caller to register a callback that will be invoked when the result of the computation is available.

A Promise is used to represent a value that is initially unknown, but is expected to be available in the future. It allows the caller to register callbacks that will be invoked when the value is available.

### Difference
The main difference between a Future and a Promise is that a Future is used to represent the result of an asynchronous computation, while a Promise is used to represent a value that is initially unknown, but is expected to be available in the future. A Future provides a way for the caller to register a callback for when the result of the computation is available, while a Promise provides a way for the caller to register callbacks for when the value is available.
