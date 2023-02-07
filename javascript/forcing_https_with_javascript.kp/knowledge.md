---
title: Check for http or https protocol in javascript, then redirect to https if necessary
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the `location.protocol` property to check if the current page is using HTTP or HTTPS and then use the `location.replace` method to force the page to use HTTPS.
---

**Contents**

[TOC]

### Step 1: Detect HTTP or HTTPS

The following code will detect if the current page is using HTTP or HTTPS:

```javascript
if (window.location.protocol === "http:") {
  // code here
} else if (window.location.protocol === "https:") {
  // code here
}
```

### Step 2: Force HTTPS

The following code will force the page to use HTTPS:

```javascript
if (window.location.protocol !== "https:") {
  window.location.href = "https:" + window.location.href.substring(window.location.protocol.length);
}
```

### Step 3: Combine the Two

The following code combines the two pieces of code to detect HTTP or HTTPS and force HTTPS:

```javascript
if (window.location.protocol === "http:") {
  window.location.href = "https:" + window.location.href.substring(window.location.protocol.length);
}
```
