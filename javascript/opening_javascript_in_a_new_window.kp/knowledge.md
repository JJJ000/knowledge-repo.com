---
title: Javascript should be opened in a new window rather than a new tab
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the window.open() method with the `target` attribute set to `\_blank`.
---

**Contents**

[TOC]

# Solution 1

Using `window.open()`:

```javascript
window.open('http://www.example.com', '_blank', 'toolbar=yes,scrollbars=yes,resizable=yes,top=500,left=500,width=400,height=400');
```

# Solution 2

Using `window.open()` and `location.href`:

```javascript
var win = window.open('', '_blank');
win.location.href = 'http://www.example.com';
```
