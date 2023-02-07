---
title: What is the procedure for scrolling to a particular element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Element.scrollIntoView() method.
---

**Contents**

[TOC]

# Using window.scrollTo

The `window.scrollTo()` method can be used to scroll an element into view.

## Syntax

```javascript
window.scrollTo(x-coord, y-coord);
```

## Parameters

| Parameter | Description                                                                                    |
| --------- | ---------------------------------------------------------------------------------------------- |
| x-coord   | is the pixel along the horizontal axis of the document that you want displayed in the upper left |
| y-coord   | is the pixel along the vertical axis of the document that you want displayed in the upper left |

## Example

```html
<div id="myDiv">My Div</div>
```

```javascript
// Get the position of the div element
var rect = document.getElementById("myDiv").getBoundingClientRect();

// Scroll to the element
window.scrollTo(rect.left, rect.top);
```
