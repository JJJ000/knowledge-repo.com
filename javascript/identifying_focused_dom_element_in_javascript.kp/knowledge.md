---
title: What dom element currently has focus?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the document.activeElement property to find which DOM element has the focus in Javascript.
---

**Contents**

[TOC]

## Get the Element

The first step in finding the DOM element that has focus is to get the element. This can be done by using the `document.activeElement` property. This property will return the element that currently has focus, or `null` if no element has focus.

## Check for Focus

Once the element has been retrieved, the next step is to check if it is actually focused. This can be done by using the `document.hasFocus()` method. This method will return `true` if the element has focus, or `false` if it does not.

## Check for TabIndex

In some cases, an element may have a `tabindex` attribute set, but still not have focus. This can be checked by using the `element.hasAttribute()` method. This method will return `true` if the element has a `tabindex` attribute, or `false` if it does not.

## Check for Visibility

Finally, it is important to check if the element is visible. This can be done by checking the `element.style.visibility` property. If the value is set to `visible`, then the element is visible and has focus. If the value is set to `hidden`, then the element is not visible and does not have focus.
