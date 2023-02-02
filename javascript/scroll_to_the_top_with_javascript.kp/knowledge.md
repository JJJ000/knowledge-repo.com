---
title: Using javascript, move to the beginning of the page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: window.scrollTo(0, 0);
---

**Contents**

[TOC]

### Method 1:

```javascript
window.scrollTo(0,0);
```

### Method 2:

```javascript
document.body.scrollTop = 0;
document.documentElement.scrollTop = 0;
```

### Method 3:

```javascript
$('html, body').animate({
    scrollTop: 0
}, 'fast');
```

### Method 4:

```javascript
$('html, body').scrollTop(0);
```
