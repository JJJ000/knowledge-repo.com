---
title: Comparing JavaScript promises rejections and throwing errors
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Reject is used to indicate a failed promise, while throw is used to indicate a general error.
---

**Contents**

[TOC]

### Reject

Reject is a method used in JavaScript Promises to reject a promise with a given reason. It is used when a promise is not fulfilled and the promise is rejected with a given reason. Reject is typically used when a promise is unable to fulfill its purpose and the promise is rejected with a given reason.

### Throw

Throw is a keyword used in JavaScript to throw an error. It is used when an error occurs in the code and it is used to throw an error to indicate that something has gone wrong. Throw is typically used when an unexpected error occurs in the code and it is used to indicate that something has gone wrong and the code needs to be debugged.
