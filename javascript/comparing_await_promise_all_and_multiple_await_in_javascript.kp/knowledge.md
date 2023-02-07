---
title: What is the distinction between using await promise.all() and multiple awaits?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Await Promise.all() waits for all promises in an array to finish before continuing, while multiple await will execute each promise one at a time.
---

**Contents**

[TOC]

**Section 1: Syntax**

Await Promise.all() is a single statement that will wait for multiple promises to resolve before continuing. It takes an array of promises as an argument, and returns an array of resolved values once all promises have been resolved.

Multiple await statements can be used to wait for multiple promises to resolve before continuing. Each await statement is used to wait for one promise to resolve before continuing.

**Section 2: Execution**

Await Promise.all() will execute all the promises in the array simultaneously, and will wait for all of them to resolve before continuing.

Multiple await statements will execute each promise one at a time, waiting for each one to resolve before continuing to the next one.

**Section 3: Error Handling**

Await Promise.all() will fail if any of the promises in the array fail to resolve.

Multiple await statements will fail if any of the promises fail to resolve, but will continue to execute the remaining promises.

**Section 4: Performance**

Await Promise.all() is more efficient than multiple await statements, as it executes all the promises in the array simultaneously, rather than one at a time. This can result in faster execution times.
