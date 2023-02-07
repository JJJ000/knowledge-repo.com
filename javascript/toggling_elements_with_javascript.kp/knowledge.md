---
title: Toggle visibility of a JavaScript element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `style.display` property to hide or show an element in JavaScript.
---

**Contents**

[TOC]

# Solution 1
Using `display` Property

The most common way of hiding an element is by setting the `display` property to `none`. This will completely hide the element, and it will not take up any space on the page.

```javascript
document.getElementById("myElement").style.display = "none";
```

# Solution 2
Using `visibility` Property

Another way of hiding an element is by setting the `visibility` property to `hidden`. This will hide the element, but it will still take up the same space on the page.

```javascript
document.getElementById("myElement").style.visibility = "hidden";
```

# Solution 3
Showing an Element

To show an element that was previously hidden, you can set the `display` or `visibility` property back to their default values.

```javascript
document.getElementById("myElement").style.display = "block";
document.getElementById("myElement").style.visibility = "visible";
```
