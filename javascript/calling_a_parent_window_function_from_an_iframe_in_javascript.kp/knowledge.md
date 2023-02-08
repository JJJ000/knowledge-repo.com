---
title: Invoking a parent window function from within an iframe
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can call a parent window function from an iframe in Javascript using the window.parent object.
---

**Contents**

[TOC]

**Section 1: Overview**

Calling a parent window function from an iframe in Javascript is a common task that developers may need to do. It allows the parent window to access functions and variables from the iframe, and vice versa. This can be useful for a variety of tasks, such as passing data from the parent window to the iframe, or for triggering a function in the parent window when an event occurs in the iframe.

**Section 2: Accessing the Parent Window**

The first step to calling a parent window function from an iframe is to access the parent window. This can be done using the `window.parent` object. This object is a reference to the parent window, and can be used to access its functions and variables.

**Section 3: Calling the Function**

Once the parent window has been accessed, the function can be called using the `window.parent.functionName()` syntax. This will call the function with the same name as the one specified in the `functionName` parameter.

**Section 4: Example**

For example, if the parent window has a function called `updateData()`, it can be called from the iframe using the following code:

```javascript
window.parent.updateData();
```
