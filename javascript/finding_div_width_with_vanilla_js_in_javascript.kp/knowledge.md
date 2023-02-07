---
title: What is the syntax for determining the width of a div using vanilla javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The width of a div can be found using the `.clientWidth` property.
---

**Contents**

[TOC]

## Get the Element

First, you must get the element you want to find the width of. This can be done in a couple of ways.

1. Using the `document.getElementById()` method:

```javascript
let element = document.getElementById('myDiv');
```

2. Using the `document.querySelector()` method:

```javascript
let element = document.querySelector('#myDiv');
```

## Get the Width

Once you have the element, you can use the `.offsetWidth` property to get the width:

```javascript
let width = element.offsetWidth;
```

## Return the Width

The `.offsetWidth` property returns the width in pixels. To return the width in other units, you can use the `.style` property:

```javascript
let width = element.style.width;
```

This will return the width of the element in whatever unit it is set to (e.g. `px`, `em`, `%`, etc.).
