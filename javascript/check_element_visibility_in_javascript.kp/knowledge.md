---
title: Determine if the element is visible on the webpage
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The visibility of an element in the DOM can be checked using the `visibility` or `display` CSS properties.
---

**Contents**

[TOC]

# Option 1

## Using jQuery

Using jQuery, you can check if an element is visible in the DOM by using the `is(":visible")` method. This method returns true if the element is visible, otherwise it returns false.

Example:

```js
if ($("#myElement").is(":visible")) {
  // Element is visible
} else {
  // Element is not visible
}
```

# Option 2

## Using JavaScript

Using JavaScript, you can check if an element is visible in the DOM by using the `getComputedStyle` method. This method returns an object containing the element's computed styles. You can then check if the element has a `display` style of `none` to determine if it is visible.

Example:

```js
const element = document.getElementById("myElement");
const style = window.getComputedStyle(element);

if (style.display === "none") {
  // Element is not visible
} else {
  // Element is visible
}
```
