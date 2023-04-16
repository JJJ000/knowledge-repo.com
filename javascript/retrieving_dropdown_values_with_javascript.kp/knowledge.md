---
title: Retrieve the chosen option from a dropdown menu using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The selected value in a dropdown list can be retrieved using the `document.getElementById()` method.
---

**Contents**

[TOC]

#### Using the `.value` Property

The `.value` property of a `<select>` element can be used to get the value of the selected option.

```javascript
let select = document.querySelector('#mySelect');
let selectedValue = select.value;
```

#### Using the `.options` Property

The `.options` property of a `<select>` element returns a collection of all the `<option>` elements contained in the element. The `.selectedIndex` property of the `<select>` element can be used to get the index of the selected option in the collection.

```javascript
let select = document.querySelector('#mySelect');
let options = select.options;
let selectedIndex = select.selectedIndex;
let selectedValue = options[selectedIndex].value;
```

#### Using the `.selectedOptions` Property

The `.selectedOptions` property of a `<select>` element returns a collection of the `<option>` elements that are selected. The value of the first element in the collection can be accessed using the `.value` property.

```javascript
let select = document.querySelector('#mySelect');
let selectedOptions = select.selectedOptions;
let selectedValue = selectedOptions[0].value;
```

#### Using the `.querySelector` Method

The `.querySelector` method can be used to select the `<option>` element that is currently selected. The value of the selected `<option>` element can be accessed using the `.value` property.

```javascript
let select = document.querySelector('#mySelect');
let selectedOption = select.querySelector('option:checked');
let selectedValue = selectedOption.value;
```
