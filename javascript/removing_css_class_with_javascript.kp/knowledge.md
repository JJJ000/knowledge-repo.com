---
title: Using javascript, delete a css class from an element without using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: document.getElementById(`elementID`).classList.remove(`className`);
---

**Contents**

[TOC]

**Section 1: Selecting the Element**

To remove a CSS class from an element with JavaScript, the first step is to select the element. This can be done using the `document.querySelector()` or `document.querySelectorAll()` methods.

**Section 2: Removing the CSS Class**

Once the element has been selected, the next step is to remove the CSS class. This can be done using the `element.classList.remove()` method.

**Section 3: Updating the CSS**

Finally, the CSS must be updated to reflect the changes. This can be done using the `element.style.cssText` or `element.style.setProperty()` methods.

**Section 4: Example**

For example, to remove the "example-class" CSS class from an element with the ID of "example-element":

```javascript
const element = document.querySelector('#example-element');
element.classList.remove('example-class');
element.style.cssText = '';
```
