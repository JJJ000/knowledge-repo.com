---
title: The error 'http.get(...).map is not a function' is encountered when using angular http get with typescript and a value of [null] is present
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The http.get() method does not return an observable, so you cannot use the map() operator on it.
---

**Contents**

[TOC]

### Solution

#### 1. Check the HTTP Client Library

The `http.get(...)` function is part of an HTTP client library such as `axios` or `request`. Make sure the library is imported correctly and that the correct version is being used.

#### 2. Check the TypeScript Configuration

The error `map is not a function` is a TypeScript error and can be caused by incorrect TypeScript configuration. Make sure the TypeScript compiler is configured correctly and that the correct version of TypeScript is being used.

#### 3. Check the TypeScript Code

The `http.get(...)` function may be called incorrectly in the TypeScript code. Make sure the function is called with the correct parameters and that the return type is being handled correctly.

#### 4. Check the JavaScript Code

The error may be caused by incorrect JavaScript code. Make sure the JavaScript code is correct and that the return type of the `http.get(...)` function is being handled correctly.
