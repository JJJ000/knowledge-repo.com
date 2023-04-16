---
title: What is the jquery method for determining which radio button is selected?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the jQuery `checked` selector to determine which radio button is selected.
---

**Contents**

[TOC]

## Get Value of Selected Radio Button

The following code will return the value of the selected radio button:

```javascript
var selectedValue = $('input[name=nameOfInput]:checked').val();
```

## Get Index of Selected Radio Button

The following code will return the index of the selected radio button:

```javascript
var selectedIndex = $('input[name=nameOfInput]:checked').index();
```

## Get Name of Selected Radio Button

The following code will return the name of the selected radio button:

```javascript
var selectedName = $('input[name=nameOfInput]:checked').attr('name');
```

## Get ID of Selected Radio Button

The following code will return the ID of the selected radio button:

```javascript
var selectedId = $('input[name=nameOfInput]:checked').attr('id');
```
