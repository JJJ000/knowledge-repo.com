---
title: What is the difference between a webpage being loaded inside an iframe and directly into a browser window?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the `window.top === window` expression to determine if a webpage is being loaded directly into the browser window or inside an iframe.
---

**Contents**

[TOC]

1. Using `window.top` 
2. Using `window.self` 
3. Using `window.frameElement` 
4. Using `window.parent` 

### 1. Using `window.top`
The `window.top` property returns the top-level window object, which is the global object for the currently running JavaScript. If the current window is the top-level window, then `window.top` is equal to `window.self`.

If the current window is inside an iframe, then `window.top` returns the top-level window object of the parent window.

To check if the current window is inside an iframe, we can compare `window.top` with `window.self`. If they are not equal, then the current window is inside an iframe.

### 2. Using `window.self`
The `window.self` property returns the current window object. It is equivalent to `window` and can be used to check if the current window is the top-level window.

If the current window is the top-level window, then `window.self` is equal to `window.top`. If the current window is inside an iframe, then `window.self` is not equal to `window.top`.

### 3. Using `window.frameElement`
The `window.frameElement` property returns the `<iframe>` element in which the current window is embedded. If the current window is the top-level window, then `window.frameElement` is `null`.

If the current window is inside an iframe, then `window.frameElement` returns the `<iframe>` element in which the current window is embedded.

### 4. Using `window.parent`
The `window.parent` property returns the parent window object of the current window. If the current window is the top-level window, then `window.parent` is equal to `window.self`.

If the current window is inside an iframe, then `window.parent` returns the parent window object of the current window.
