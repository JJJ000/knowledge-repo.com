---
title: A critical issue has been encountered poor garbage collection near the memory boundary. allocation has failed due to the JavaScript memory being exhausted in ionic 3
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Increase the memory limit for Node.js to resolve the JavaScript heap out of memory error in Ionic 3.
---

**Contents**

[TOC]

# Overview
When running an Ionic 3 application in JavaScript, a "FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory" error can occur. This error occurs when the JavaScript heap has been exhausted and there is not enough memory for the application to continue running. This error can be caused by a variety of factors, including memory leaks, inefficient code, and excessive memory usage.

# Causes
Memory leaks can be a major cause of this error. A memory leak occurs when an application allocates memory for an object, but then fails to release it when the object is no longer needed. This can cause the application to use up more and more memory until it eventually runs out of memory.

Inefficient code can also lead to this error. If an application is making too many unnecessary calls to the JavaScript engine, or is not properly releasing memory, it can cause the JavaScript heap to be exhausted.

Excessive memory usage can also be a cause of this error. If an application is attempting to use more memory than is available, it can cause the JavaScript heap to be exhausted.

# Solutions
The first step in resolving this error is to identify the cause. If a memory leak is the cause, then it should be addressed by identifying and fixing the source of the leak. If inefficient code is the cause, then the code should be refactored to be more efficient. If excessive memory usage is the cause, then the application should be optimized to use less memory.

Once the cause of the error has been identified, the next step is to address the issue. If a memory leak is the cause, then the source of the leak should be identified and fixed. If inefficient code is the cause, then the code should be refactored to be more efficient. If excessive memory usage is the cause, then the application should be optimized to use less memory.

Finally, if the cause of the error is still not identified, then the application should be monitored to identify the source of the issue. This can be done by using a memory profiler to identify which objects are consuming the most memory, and then addressing those objects to reduce their memory usage.
