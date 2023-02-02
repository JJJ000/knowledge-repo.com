---
title: What is the process for attaching a class to a specified element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To add a class to a given element in Javascript, use the element`s .classList.add() method.
---

**Contents**

[TOC]

# Section 1: Select the Element

The first step in adding a class to an element is to select the element. This can be done using the `document.querySelector()` method. This method takes a CSS selector as an argument and returns the first element that matches the selector.

# Section 2: Add the Class

Once the element has been selected, the class can be added using the `classList.add()` method. This method takes a class name as an argument and adds it to the element's class list.

# Section 3: Check for Existing Classes

Before adding a class to an element, it is important to check if the class already exists on the element. This can be done using the `classList.contains()` method. This method takes a class name as an argument and returns `true` if the class is found on the element, and `false` if it is not.

# Section 4: Remove Existing Classes

If the class already exists on the element, it can be removed using the `classList.remove()` method. This method takes a class name as an argument and removes it from the element's class list.
