---
title: What is the jquery command to select the focused element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the $(`focus`) selector to get the focused element with jQuery.
---

**Contents**

[TOC]

## Using jQuery

jQuery provides a convenient way to get the focused element using the `:focus` selector.

```javascript
var focusedElement = $(':focus');
```

## Using document.activeElement

Another way to get the focused element is to use the `document.activeElement` property.

```javascript
var focusedElement = document.activeElement;
```

## Using document.querySelector

You can also use the `document.querySelector` method to get the focused element.

```javascript
var focusedElement = document.querySelector(':focus');
```

## Using document.getElementById

Finally, you can use the `document.getElementById` method to get the focused element.

```javascript
var focusedElement = document.getElementById('focused-element-id');
```
