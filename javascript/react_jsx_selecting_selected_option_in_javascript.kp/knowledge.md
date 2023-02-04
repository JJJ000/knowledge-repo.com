---
title: Selecting the "selected" attribute on a <select> option that has already been chosen
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: In React JSX, you can set the `selected` attribute on the <select> element`s <option> element to true to select a particular option.
---

**Contents**

[TOC]

### Using the "selected" Attribute

The `selected` attribute can be used to pre-select an option in a `<select>` element. When the attribute is included in the `<option>` element, that option will be selected by default when the page is first loaded.

```html
<select>
  <option value="volvo" selected>Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
```

### Using JavaScript

The `selected` attribute can also be used in combination with JavaScript to select an option in a `<select>` element. The `selectedIndex` property of the `<select>` element can be used to set the index of the option to be selected.

```javascript
// Get the <select> element
let select = document.getElementById("mySelect");

// Set the selected index
select.selectedIndex = 2;
```

### Using jQuery

Using jQuery, the `.prop()` method can be used to set the `selected` attribute of an option.

```javascript
// Select the option with the value "volvo"
$('#mySelect option[value="volvo"]').prop('selected', true);
```

### Using React

In React, the `value` prop of the `<select>` element can be used to set the selected option.

```javascript
<select value="volvo">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
```
