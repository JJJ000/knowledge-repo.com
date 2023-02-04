---
title: Determine if the device is running ios
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can detect if a device is iOS by checking the user agent of the browser.
---

**Contents**

[TOC]

## Solution 1

Using `navigator.userAgent`:

```js
if (navigator.userAgent.match(/iPhone|iPad|iPod/i)) {
  // Device is an iOS device
}
```

## Solution 2

Using `navigator.platform`:

```js
if (navigator.platform.match(/iPhone|iPad|iPod/i)) {
  // Device is an iOS device
}
```

## Solution 3

Using `navigator.appVersion`:

```js
if (navigator.appVersion.match(/iPhone|iPad|iPod/i)) {
  // Device is an iOS device
}
```

## Solution 4

Using `navigator.userAgent` and `navigator.platform`:

```js
if (navigator.userAgent.match(/iPhone|iPad|iPod/i) || 
    navigator.platform.match(/iPhone|iPad|iPod/i)) {
  // Device is an iOS device
}
```
