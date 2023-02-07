---
title: Retrieving clipboard data with JavaScript when a paste event occurs (works on multiple browsers)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The ClipboardEvent.clipboardData property can be used to access the clipboard data in a paste event in a cross-browser compatible way.
---

**Contents**

[TOC]

# Section 1: Overview
The clipboard is an essential part of any computer's user interface, allowing users to quickly copy and paste data from one application to another. In JavaScript, the clipboard can be accessed and manipulated using the Clipboard API, which is supported in all modern browsers.

# Section 2: The Clipboard API
The Clipboard API provides a set of methods and events that allow developers to interact with the system clipboard. The most commonly used method is the `getData()` method, which retrieves data from the clipboard. When a user pastes data into a web page, the `paste` event is triggered, allowing developers to access the data using the `getData()` method.

# Section 3: Cross-Browser Compatibility
The Clipboard API is supported in all modern browsers, including Chrome, Firefox, Safari, and Edge. However, the API is not supported in Internet Explorer, so developers must use a polyfill or alternative solution to access clipboard data in IE.

# Section 4: Example
Here is an example of how to access clipboard data when a user pastes data into a web page:

```javascript
document.addEventListener('paste', (event) => {
  const clipboardData = event.clipboardData || window.clipboardData;
  const data = clipboardData.getData('text/plain');
  console.log(data);
});
```
