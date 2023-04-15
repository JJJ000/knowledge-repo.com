---
title: How can I obtain the current url using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The current URL can be retrieved using the window.location.href property.
---

**Contents**

[TOC]

### Solution

### Using `window.location`

The current URL can be retrieved using the `window.location` object.

```javascript
let currentURL = window.location.href;
```

### Using `document.URL`

The current URL can also be retrieved using the `document.URL` property.

```javascript
let currentURL = document.URL;
```
