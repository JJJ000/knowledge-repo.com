---
title: Stop body from moving when a modal is activated
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using `overflow hidden` on the body element will prevent the body from scrolling when a modal is opened.
---

**Contents**

[TOC]

### Method 1

Use `overflow: hidden` on the `body` element when the modal is opened.

```javascript
const openModal = () => {
  document.body.style.overflow = 'hidden';
};

const closeModal = () => {
  document.body.style.overflow = 'visible';
};
```

### Method 2

Use `position: fixed` on the `body` element when the modal is opened.

```javascript
const openModal = () => {
  document.body.style.position = 'fixed';
};

const closeModal = () => {
  document.body.style.position = 'relative';
};
```
