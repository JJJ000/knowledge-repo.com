---
title: Retrieve the class name using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The class name can be retrieved using the jQuery method `$(selector).attr(`class`)`.
---

**Contents**

[TOC]

## Method 1
Using the `prop()` method:

```javascript
var className = $(selector).prop('className');
```

## Method 2
Using the `attr()` method:

```javascript
var className = $(selector).attr('class');
```

## Method 3
Using the `className` property:

```javascript
var className = $(selector)[0].className;
```

## Method 4
Using the `classList` property:

```javascript
var className = $(selector)[0].classList.value;
```
