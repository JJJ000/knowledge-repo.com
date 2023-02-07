---
title: What is the method for determining the version of a browser?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can detect the version of a browser in Javascript by using the navigator.appVersion property.
---

**Contents**

[TOC]

### Using navigator.userAgent

The `navigator.userAgent` property returns a string containing information about the user's browser. This string can be parsed to detect the browser version.

### Example

```javascript
let userAgent = navigator.userAgent;
let version = userAgent.match(/Chrome\/(\d+)/);

// version[1] contains the version number
let chromeVersion = version[1];
```

### Using feature detection

Another approach is to use feature detection. This involves checking for the presence of features that are specific to a certain browser version.

### Example

```javascript
// Check for support of the new ES6 features
if ('Promise' in window) {
  // The browser supports the ES6 features
  console.log('Browser is at least Chrome version 42 or higher');
}
```
