---
title: What is the process for sending someone to a different web page?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the window.location.href or window.location.replace methods to redirect to another webpage in Javascript.
---

**Contents**

[TOC]

### Using `window.location`

The `window.location` object can be used to get the current page address (URL) and to redirect the browser to a new page. To redirect the browser to a new page, we can set `window.location.href` to the new URL.

```javascript
window.location.href = "http://www.example.com";
```

### Using `window.location.replace()`

The `window.location.replace()` method replaces the current document with a new page. This method is similar to `window.location.href`, but `window.location.replace()` removes the current page from the session history, meaning that the user won't be able to use the back button to navigate to the original page.

```javascript
window.location.replace("http://www.example.com");
```

### Using `window.location.assign()`

The `window.location.assign()` method loads a new document. This method is similar to `window.location.href`, but `window.location.assign()` adds the new page to the session history, meaning that the user will be able to use the back button to navigate to the original page.

```javascript
window.location.assign("http://www.example.com");
```

### Using `document.location`

The `document.location` object is an alias for `window.location`. It can be used to get the current page address (URL) and to redirect the browser to a new page. To redirect the browser to a new page, we can set `document.location.href` to the new URL.

```javascript
document.location.href = "http://www.example.com";
```
