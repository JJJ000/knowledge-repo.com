---
title: Find the height of a div using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The height of a div can be retrieved using the `offsetHeight` property of the element.
---

**Contents**

[TOC]

### Method 1 - Using `offsetHeight`

The `offsetHeight` property of a DOM element can be used to get the height of the element.

```javascript
let element = document.getElementById('myElement');
let height = element.offsetHeight;
```

### Method 2 - Using `getBoundingClientRect()`

The `getBoundingClientRect()` method of a DOM element can be used to get the height of the element.

```javascript
let element = document.getElementById('myElement');
let rect = element.getBoundingClientRect();
let height = rect.height;
```

### Method 3 - Using `clientHeight`

The `clientHeight` property of a DOM element can be used to get the height of the element.

```javascript
let element = document.getElementById('myElement');
let height = element.clientHeight;
```

### Method 4 - Using `scrollHeight`

The `scrollHeight` property of a DOM element can be used to get the height of the element.

```javascript
let element = document.getElementById('myElement');
let height = element.scrollHeight;
```
