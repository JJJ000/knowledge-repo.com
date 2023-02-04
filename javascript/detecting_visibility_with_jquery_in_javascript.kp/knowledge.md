---
title: Determine if an element is visible using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery`s .is(`visible`) method can be used to detect if an element is visible.
---

**Contents**

[TOC]

#1. Check for Visibility

The most reliable way to check if an element is visible with jQuery is to use the `is(':visible')` method. This method will return `true` if the element is visible, and `false` if it is not.

#2. Check for Display Property

Another way to check if an element is visible with jQuery is to check the `display` property of the element. If the `display` property is set to `none`, then the element is not visible.

#3. Check for Visibility in Parent Element

It is also important to check the visibility of the parent element of the element in question. If the parent element is not visible, then the element itself cannot be visible.

#4. Consider Other Factors

Finally, it is important to consider other factors such as opacity and visibility of the element, as well as the visibility of any other elements that may be overlaying the element.
