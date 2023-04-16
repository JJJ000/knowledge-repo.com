---
title: Determine the dimensions of the screen, the webpage currently being viewed, and the browser window
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The size of the screen, current web page, and browser window can be retrieved in JavaScript using the window.innerWidth, window.innerHeight, document.documentElement.clientWidth, and document.documentElement.clientHeight properties.
---

**Contents**

[TOC]

## Screen Size

The `window.screen` object can be used to get the size of the user's screen in pixels.

```javascript
var width = window.screen.width;
var height = window.screen.height;
```

## Web Page Size

The `document.documentElement` object can be used to get the size of the current web page in pixels.

```javascript
var width = document.documentElement.clientWidth;
var height = document.documentElement.clientHeight;
```

## Browser Window Size

The `window.innerWidth` and `window.innerHeight` properties can be used to get the size of the browser window in pixels.

```javascript
var width = window.innerWidth;
var height = window.innerHeight;
```
