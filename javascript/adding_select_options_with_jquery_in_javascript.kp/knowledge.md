---
title: How can I use jquery to add options to a <select> element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: jQuery can be used to add options to a <select> element in Javascript by using the .append() method.
---

**Contents**

[TOC]

#### 1. Create the Option Element

Using jQuery, you can create a new `<option>` element and set its attributes. The following example creates an `<option>` element with the value "volvo" and the text "Volvo":

```javascript
$('<option>', {
    value: 'volvo',
    text : 'Volvo'
}).appendTo('#selectElement');
```

#### 2. Append the Option Element

Once the `<option>` element has been created, it can be appended to the `<select>` element using the `appendTo()` method. The following example appends the `<option>` element to the `<select>` element with the id "selectElement":

```javascript
$('<option>', {
    value: 'volvo',
    text : 'Volvo'
}).appendTo('#selectElement');
```

#### 3. Create Multiple Options

You can also create multiple `<option>` elements and append them to the `<select>` element by using a loop. The following example creates three `<option>` elements and appends them to the `<select>` element with the id "selectElement":

```javascript
var options = [
    { value: 'audi', text : 'Audi' },
    { value: 'bmw', text : 'BMW' },
    { value: 'volvo', text : 'Volvo' }
];

for (var i = 0; i < options.length; i++) {
    $('<option>', {
        value: options[i].value,
        text : options[i].text
    }).appendTo('#selectElement');
}
```

#### 4. Add Options to a Specific Index

If you want to add the `<option>` elements to a specific index in the `<select>` element, you can use the `eq()` method to select the index and the `before()` or `after()` method to insert the `<option>` element. The following example adds an `<option>` element with the value "mercedes" and the text "Mercedes" to the second index in the `<select>` element with the id "selectElement":

```javascript
$('<option>', {
    value: 'mercedes',
    text : 'Mercedes'
}).insertAfter('#selectElement option:eq(1)');
```
