---
title: What is the current location of the mouse cursor without using any mouse events?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: It is not possible to get the mouse position without events (without moving the mouse) in Javascript.
---

**Contents**

[TOC]

**Option 1: Using the Window Object**

1. Access the `window` object.
2. Use the `window.screenX` and `window.screenY` properties.

**Option 2: Using the Document Object**

1. Access the `document` object.
2. Use the `document.documentElement.clientX` and `document.documentElement.clientY` properties.

**Option 3: Using the Navigator Object**

1. Access the `navigator` object.
2. Use the `navigator.geolocation.getCurrentPosition` method.

**Option 4: Using the Element Object**

1. Access the `element` object.
2. Use the `element.getBoundingClientRect` method.
