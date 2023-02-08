---
title: What is the code to scroll to an element using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the Element.scrollIntoView() method to scroll to an element in JavaScript.
---

**Contents**

[TOC]

## Method 1: Using Element.scrollIntoView()
This method is used to scroll the element into view. It takes an optional parameter which allows you to specify whether the element should be scrolled into the top or bottom of the viewport.

Syntax:
```
element.scrollIntoView(alignToTop);
```

Example:
```
let element = document.getElementById("myElement");
element.scrollIntoView(true);
```

## Method 2: Using Window.scrollTo()
This method is used to scroll the window to a particular place in the document. It takes two parameters, the first parameter specifies the horizontal coordinate and the second parameter specifies the vertical coordinate.

Syntax:
```
window.scrollTo(xpos, ypos);
```

Example:
```
let element = document.getElementById("myElement");
let position = element.getBoundingClientRect();
window.scrollTo(position.left, position.top);
```

## Method 3: Using Element.scrollTop
This method is used to scroll the element to a specified position. It takes one parameter which specifies the position to scroll to.

Syntax:
```
element.scrollTop = position;
```

Example:
```
let element = document.getElementById("myElement");
let position = element.getBoundingClientRect();
element.scrollTop = position.top;
```

## Method 4: Using Element.scrollBy()
This method is used to scroll the element by a specified amount. It takes two parameters, the first parameter specifies the amount to scroll horizontally and the second parameter specifies the amount to scroll vertically.

Syntax:
```
element.scrollBy(x, y);
```

Example:
```
let element = document.getElementById("myElement");
let position = element.getBoundingClientRect();
element.scrollBy(0, position.top);
```
