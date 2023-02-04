---
title: The fetch function has not been declared or defined
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: fetch is a web API used for making network requests, which is not natively available in JavaScript.
---

**Contents**

[TOC]

# Solution

## What is a ReferenceError? 
A ReferenceError is a type of error that occurs when the code references a variable or object that does not exist. This type of error occurs when a variable or object is not defined, or when a function is used without being declared.

## What is fetch? 
Fetch is an API used for making network requests. It is a modern way to make HTTP requests, and allows for more control over the request and response than traditional methods such as XMLHttpRequest.

## Why is fetch not defined? 
Fetch is not defined because it is not part of the core JavaScript language. It is a web API, which means it is not part of the language, but is instead provided by the browser.

## How to use fetch? 
In order to use fetch, you must first include a polyfill or use a modern browser that supports the API. Once the API is available, you can use the fetch() method to make a request. The fetch() method takes two arguments, the URL of the request and an object containing the request options. Once the request is made, the response can be handled using the then() or catch() methods.
