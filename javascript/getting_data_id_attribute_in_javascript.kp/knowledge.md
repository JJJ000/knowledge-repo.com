---
title: What is the method for obtaining the data-id attribute?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can get the data-id attribute in Javascript using the `getAttribute()` method.
---

**Contents**

[TOC]

## Option 1: Using getAttribute()

The `getAttribute()` method can be used to get the value of any attribute on an element. 

Syntax: 

```
element.getAttribute(attribute)
```

Example:

```
var dataID = document.getElementById("myElement").getAttribute("data-id");
```

## Option 2: Using dataset

The `dataset` property can be used to access all the custom data attributes (data-*) set on the element. 

Syntax: 

```
element.dataset.attribute
```

Example: 

```
var dataID = document.getElementById("myElement").dataset.id;
```
