---
title: What is the JavaScript code to take out the hash from the window.location (url) without reloading the page?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `history.pushState()` method to update the URL without reloading the page.
---

**Contents**

[TOC]

**Solution 1 - Using window.history.pushState()**

1. Create a new URL object with the desired URL string.

```javascript
var newURL = new URL(window.location.href);
```

2. Remove the hash from the URL object.

```javascript
newURL.hash = '';
```

3. Update the browser history using window.history.pushState() with the new URL object.

```javascript
window.history.pushState({}, document.title, newURL);
```

**Solution 2 - Using window.location.replace()**

1. Create a new URL object with the desired URL string.

```javascript
var newURL = new URL(window.location.href);
```

2. Remove the hash from the URL object.

```javascript
newURL.hash = '';
```

3. Replace the current URL with the new URL using window.location.replace().

```javascript
window.location.replace(newURL);
```
