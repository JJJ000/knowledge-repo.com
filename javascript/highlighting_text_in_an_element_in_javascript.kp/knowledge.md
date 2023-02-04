---
title: Highlighting text within an element, similar to what you would do with a mouse
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the window.getSelection() method to select text in an element in JavaScript.
---

**Contents**

[TOC]

**1. Get Element**

The first step is to get the element that you want to select the text from. This can be done by using the `document.getElementById()` or `document.querySelector()` methods. These methods will return the element that you have selected.

**2. Create Range**

Once the element has been selected, the next step is to create a range object. This can be done by using the `document.createRange()` method. This method will return a range object which can then be used to select text within the element.

**3. Select Text**

Once the range object has been created, the next step is to select the text within the element. This can be done by using the `range.selectNodeContents()` method. This method will select all of the text within the element.

**4. Set Selection**

Finally, the last step is to set the selection. This can be done by using the `window.getSelection()` method. This method will return a selection object which can then be used to set the selection. This can be done by using the `selection.addRange()` method.
