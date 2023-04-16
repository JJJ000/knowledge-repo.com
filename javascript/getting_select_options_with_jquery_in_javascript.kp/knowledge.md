---
title: What is the best way to retrieve all of the options of a select element using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the jQuery `.find(`option`)` method to get all options of a select element.
---

**Contents**

[TOC]

## Solution 1

Using the `.find()` method:

```javascript
var selectOptions = $("#mySelect").find("option");
```

## Solution 2

Using the `.children()` method:

```javascript
var selectOptions = $("#mySelect").children("option");
```

## Solution 3

Using the `.map()` method:

```javascript
var selectOptions = $("#mySelect").map(function() {
  return $(this).find("option");
});
```

## Solution 4

Using the `.each()` method:

```javascript
var selectOptions = [];
$("#mySelect").each(function(){
  selectOptions.push($(this).find("option"));
});
```
