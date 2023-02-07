---
title: Set the css property visibility to hidden, equivalent to jquery .hide()
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: document.element.style.visibility = `hidden`;
---

**Contents**

[TOC]

1. Setting Visibility with CSS
--------------------------------

The most straightforward way to hide an element with JavaScript is to set its CSS `visibility` property to `hidden`. This can be done directly in the style attribute of the element, or by setting a class on the element and defining the visibility in a stylesheet.

```html
<div id="myDiv" style="visibility: hidden;">
  This div is hidden.
</div>
```

2. Setting Visibility with JavaScript
------------------------------------

Alternatively, you can set the `visibility` property of an element using JavaScript. This can be done using the `style` property of an element, or by setting a class on the element and defining the visibility in a stylesheet.

```javascript
let myDiv = document.getElementById('myDiv');
myDiv.style.visibility = 'hidden';
```

3. Setting Visibility with jQuery
---------------------------------

In jQuery, the `.hide()` method can be used to set the `visibility` property of an element to `hidden`.

```javascript
$('#myDiv').hide();
```

4. Setting Visibility with the jQuery `.css()` Method
---------------------------------------------------

The jQuery `.css()` method can also be used to set the `visibility` property of an element to `hidden`.

```javascript
$('#myDiv').css('visibility', 'hidden');
```
