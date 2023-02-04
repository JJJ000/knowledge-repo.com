---
title: What is the process for deselecting a radio button?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `checked` property of the radio button element and set it to false.
---

**Contents**

[TOC]

## Using `checked` Property 

The `checked` property of a radio button can be used to uncheck it. 

The following example shows how to uncheck a radio button using the `checked` property.

```javascript
// Get the radio button
var radioButton = document.getElementById("radio-button-id");

// Uncheck the radio button
radioButton.checked = false;
```

## Using `defaultChecked` Property 

The `defaultChecked` property of a radio button can be used to uncheck it. 

The following example shows how to uncheck a radio button using the `defaultChecked` property.

```javascript
// Get the radio button
var radioButton = document.getElementById("radio-button-id");

// Uncheck the radio button
radioButton.defaultChecked = false;
```
