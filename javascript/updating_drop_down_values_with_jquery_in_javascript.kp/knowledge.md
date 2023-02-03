---
title: Use jquery to alter the chosen option in a drop-down menu
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: $(`#dropdownID`).val(`newValue`);
---

**Contents**

[TOC]

### Step 1: Create a Drop-Down List

Create a drop-down list in HTML with the `<select>` element, and populate it with `<option>` elements to define the available options:

```html
<select id="myDropdown">
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
  <option value="3">Option 3</option>
</select>
```

### Step 2: Select an Option

To select an option in the drop-down list, use the jQuery `val()` method:

```javascript
$('#myDropdown').val('2');
```

This will select the second option with the value `2`.

### Step 3: Listen for Changes

To listen for changes in the drop-down list, use the jQuery `change()` method:

```javascript
$('#myDropdown').change(function() {
  // Do something when the selected value changes
});
```

### Step 4: Get the Selected Value

To get the selected value of the drop-down list, use the jQuery `val()` method:

```javascript
var selectedValue = $('#myDropdown').val();
```
