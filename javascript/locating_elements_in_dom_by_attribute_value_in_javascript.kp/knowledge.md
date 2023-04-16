---
title: Search for an element in the document object model (dom) using an attribute value
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: document.querySelector(`[attribute=`value`]`) can be used to find an element in the DOM based on an attribute value.
---

**Contents**

[TOC]

**Section 1: Accessing Elements with getElementsByAttribute()**

The `getElementsByAttribute()` method can be used to access elements in the DOM based on an attribute value. It takes two parameters, the attribute name and the attribute value. It returns an array of elements that match the criteria.

**Section 2: Using the for Loop**

In order to access a single element from the array that is returned by the `getElementsByAttribute()` method, we can use a `for` loop to iterate over the array. Inside the loop, we can check the attribute value of each element to see if it matches the one that we are looking for. If it does, we can store that element in a variable.

**Section 3: Using querySelector()**

Another way to access an element in the DOM based on an attribute value is to use the `querySelector()` method. This method takes a CSS selector as a parameter, and it returns the first element that matches the selector. To access an element based on an attribute value, we can use the attribute selector syntax, which looks like this: `[attributeName="attributeValue"]`.

**Section 4: Using querySelectorAll()**

If we want to access multiple elements in the DOM based on an attribute value, we can use the `querySelectorAll()` method. This method takes a CSS selector as a parameter, and it returns an array of all elements that match the selector. To access elements based on an attribute value, we can use the attribute selector syntax, which looks like this: `[attributeName="attributeValue"]`.
