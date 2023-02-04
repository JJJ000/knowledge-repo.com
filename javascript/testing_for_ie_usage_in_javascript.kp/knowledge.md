---
title: Verify if the user is utilizing internet explorer
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can check if a user is using IE by checking the user`s navigator.userAgent property.
---

**Contents**

[TOC]

### Solution

#### Using User Agent

We can use the `navigator.userAgent` property to detect the user's browser.

```javascript
if (navigator.userAgent.indexOf("MSIE") != -1) {
    console.log("User is using IE");
}
```

#### Using MSIE Detection

We can also check for the presence of the `MSIE` string in the `navigator.appVersion` property.

```javascript
if (navigator.appVersion.indexOf("MSIE") != -1) {
    console.log("User is using IE");
}
```

#### Using Trident Detection

We can also check for the presence of the `Trident` string in the `navigator.userAgent` property.

```javascript
if (navigator.userAgent.indexOf("Trident") != -1) {
    console.log("User is using IE");
}
```

#### Using Edge Detection

We can also check for the presence of the `Edge` string in the `navigator.userAgent` property.

```javascript
if (navigator.userAgent.indexOf("Edge") != -1) {
    console.log("User is using IE");
}
```
