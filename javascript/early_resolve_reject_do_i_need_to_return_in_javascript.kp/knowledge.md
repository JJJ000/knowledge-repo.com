---
title: Should I come back after resolving or rejecting the issue early?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, you do not need to return after early resolve/reject in Javascript.
---

**Contents**

[TOC]

**Yes**

**Section 1: Why Return is Necessary**

When using the Promise API in JavaScript, it is important to return the promise after resolving or rejecting it. This ensures that the promise is properly handled and that any errors are caught and handled correctly. Without returning the promise, the code that calls the promise may not be able to properly handle the result of the promise and may not be able to properly handle any errors that may occur.

**Section 2: How To Return The Promise**

Returning the promise is simple. After resolving or rejecting the promise, simply add a return statement and return the promise. This will ensure that the promise is properly handled and any errors are caught and handled correctly.

**Section 3: Benefits Of Returning The Promise**

Returning the promise ensures that the code that calls the promise is able to properly handle the result of the promise. This helps to make sure that any errors that may occur are caught and handled correctly. Additionally, returning the promise helps to make sure that the code that calls the promise is able to properly handle any changes to the promise state.

**Section 4: Conclusion**

Returning the promise after resolving or rejecting it is an important part of using the Promise API in JavaScript. It ensures that the code that calls the promise is able to properly handle the result of the promise and any errors that may occur. Additionally, it helps to make sure that the code that calls the promise is able to properly handle any changes to the promise state.
