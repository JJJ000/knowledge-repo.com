---
title: What is the syntax for selecting an element by name using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can select an element by name with jQuery using the syntax `$(`[name=`name`]`)`.
---

**Contents**

[TOC]

## Selecting by Name

The jQuery `.attr()` method can be used to select an element by name.

```javascript
$('[name="name"]');
```

## Setting the Name Attribute

The `.attr()` method can also be used to set the name attribute of an element.

```javascript
$('#myElement').attr('name', 'name');
```

## Using the Name Selector

The jQuery `[name="name"]` selector can be used to select an element by name.

```javascript
$('[name="name"]');
```

## Setting the Name Selector

The `.attr()` method can also be used to set the name attribute of an element.

```javascript
$('#myElement').attr('name', 'name');
```
