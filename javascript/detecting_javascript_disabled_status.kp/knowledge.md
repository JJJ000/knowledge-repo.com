---
title: What are signs that JavaScript has been disabled?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: It is not possible to detect if JavaScript is disabled in JavaScript.
---

**Contents**

[TOC]

# Section 1: Check for Element Visibility

One way to detect if JavaScript is disabled is by checking if an element is visible. This can be done by using the `getComputedStyle` method to check the `visibility` property of an element.

```javascript
var el = document.getElementById("myElement");

if (window.getComputedStyle(el).visibility === "hidden") {
  // JavaScript is disabled
}
```

# Section 2: Check for Script Tags

Another way to detect if JavaScript is disabled is by checking for the presence of script tags. This can be done by using the `querySelectorAll` method to check for `script` elements on the page.

```javascript
if (document.querySelectorAll("script").length === 0) {
  // JavaScript is disabled
}
```

# Section 3: Check for Cookies

A third way to detect if JavaScript is disabled is by checking for cookies. This can be done by using the `getCookie` method to check for the presence of a cookie.

```javascript
if (getCookie("js") === "disabled") {
  // JavaScript is disabled
}
```

# Section 4: Check for AJAX

A fourth way to detect if JavaScript is disabled is by checking for AJAX requests. This can be done by using the `XMLHttpRequest` object to check for the presence of an AJAX request.

```javascript
if (window.XMLHttpRequest === undefined) {
  // JavaScript is disabled
}
```
