---
title: What are the dimensions of the browser viewport?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The browser viewport dimensions can be retrieved using the `window.innerWidth` and `window.innerHeight` properties.
---

**Contents**

[TOC]

#### Using Window Object

The window object provides information about the browser viewport size in the `innerWidth` and `innerHeight` properties.

```javascript
var viewportWidth = window.innerWidth;
var viewportHeight = window.innerHeight;
```

#### Using Document Object

The document object provides information about the browser viewport size in the `documentElement.clientWidth` and `documentElement.clientHeight` properties.

```javascript
var viewportWidth = document.documentElement.clientWidth;
var viewportHeight = document.documentElement.clientHeight;
```

#### Using Media Queries

We can use CSS media queries to determine the browser viewport size.

```css
@media only screen and (max-width: 600px) {
  /* viewport is less than 600px wide */
}

@media only screen and (min-width: 600px) {
  /* viewport is at least 600px wide */
}
```

#### Using jQuery

We can use jQuery to get the browser viewport size.

```javascript
var viewportWidth = $(window).width();
var viewportHeight = $(window).height();
```
