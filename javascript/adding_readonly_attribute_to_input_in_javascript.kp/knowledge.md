---
title: What is the syntax to make an <input> element read-only?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To add a `readonly` attribute to an <input> in Javascript, use the .setAttribute() method with the attribute name `readonly` and a value of `true`.
---

**Contents**

[TOC]

**Solution 1:**

Using the `readOnly` Property
--------------------------------

The `readOnly` property of an `<input>` element can be used to set it to read-only. This can be done using the following syntax:

```javascript
document.getElementById("inputID").readOnly = true;
```

**Solution 2:**

Using the `setAttribute()` Method
--------------------------------

The `setAttribute()` method can also be used to set an `<input>` element to read-only. This can be done using the following syntax:

```javascript
document.getElementById("inputID").setAttribute("readonly", "readonly");
```
