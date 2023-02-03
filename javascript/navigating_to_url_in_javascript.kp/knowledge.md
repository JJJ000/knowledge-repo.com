---
title: How to make the browser go to a url using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the window.location object to set the window`s URL to the desired URL.
---

**Contents**

[TOC]

### Using the Location Object

The `location` object can be used to get the current URL and also to redirect the browser to a different URL. To redirect the browser to a different page, we can use the `location.href` property.

```javascript
location.href = "http://www.example.com";
```

### Using the Window Object

The `window` object also provides a `location` property, which can be used to navigate to a different URL.

```javascript
window.location = "http://www.example.com";
```

### Using the Window.location.replace() Method

The `window.location.replace()` method can be used to replace the current document with a new one.

```javascript
window.location.replace("http://www.example.com");
```

### Using the Window.location.assign() Method

The `window.location.assign()` method can be used to load a new document.

```javascript
window.location.assign("http://www.example.com");
```
