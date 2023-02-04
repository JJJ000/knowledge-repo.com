---
title: Changing the location of a webpage in JavaScript using a relative url
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: window.location.href can be used to redirect to a relative URL in JavaScript.
---

**Contents**

[TOC]

## Using the window.location Object
We can use the `window.location` object to redirect to a relative URL in JavaScript. The `window.location` object contains information about the current URL and can be used to redirect to a relative URL by setting the `window.location.href` property to the relative URL.

## Example
For example, if we wanted to redirect to a relative URL of `/mypage.html`, we could use the following code:

```js
window.location.href = '/mypage.html';
```

## Using the window.location.replace() Method
We can also use the `window.location.replace()` method to redirect to a relative URL. This method is similar to the `window.location.href` property, but it replaces the current page in the history instead of creating a new entry.

## Example
For example, if we wanted to redirect to a relative URL of `/mypage.html`, we could use the following code:

```js
window.location.replace('/mypage.html');
```
