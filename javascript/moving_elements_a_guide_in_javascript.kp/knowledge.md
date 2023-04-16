---
title: How to insert an element into another element
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the appendChild() method to move an element into another element in Javascript.
---

**Contents**

[TOC]

# Section 1: Select the Element

The first step is to select the element that you want to move. You can do this using the `document.querySelector()` method, which takes a CSS selector as an argument and returns the first element that matches the selector.

# Section 2: Create a Reference to the Element

Once you have selected the element you want to move, you will need to create a reference to it. This can be done by assigning the element to a variable, such as `var element = document.querySelector("#myElement");`.

# Section 3: Append the Element to the New Parent

Once you have a reference to the element, you can append it to the new parent element with the `appendChild()` method. This method takes the element as an argument and adds it as a child of the parent element.

# Section 4: Remove the Element from the Original Parent

Finally, you can remove the element from the original parent with the `removeChild()` method. This method takes the element as an argument and removes it from the parent element.
