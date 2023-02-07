---
title: What is the process for copying text to the clipboard in reactjs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To copy text to the clipboard in ReactJS, use the `navigator.clipboard.writeText()` method.
---

**Contents**

[TOC]

##### Using the Clipboard API

The Clipboard API provides the ability to respond to user-initiated copy and paste operations, as well as to asynchronously read from and write to the system clipboard. To copy text to the clipboard, we can use the `writeText()` method.

```javascript
navigator.clipboard.writeText(text).then(function() {
  console.log('Async: Copying to clipboard was successful!');
}, function(err) {
  console.error('Async: Could not copy text: ', err);
});
```

##### Using the execCommand

We can also use the `execCommand()` method to copy text to the clipboard. This method is supported by most modern browsers.

```javascript
function copyToClipboard(text) {
  var dummy = document.createElement("textarea");
  document.body.appendChild(dummy);
  dummy.value = text;
  dummy.select();
  document.execCommand("copy");
  document.body.removeChild(dummy);
}
```
