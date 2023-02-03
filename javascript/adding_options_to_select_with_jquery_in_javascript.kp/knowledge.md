---
title: What is the most effective way to use jquery to populate a select element with options from a JavaScript object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The best way to add options to a select from a JavaScript object with jQuery is to use the .append() method.
---

**Contents**

[TOC]

##### Option 1:
Using `.append()`:

```javascript
var select = $('#select');

for (var key in obj) {
    if (obj.hasOwnProperty(key)) {
        select.append('<option value="' + key + '">' + obj[key] + '</option>');
    }
}
```

##### Option 2:
Using `.html()`:

```javascript
var select = $('#select');
var options = '';

for (var key in obj) {
    if (obj.hasOwnProperty(key)) {
        options += '<option value="' + key + '">' + obj[key] + '</option>';
    }
}

select.html(options);
```

##### Option 3:
Using `.append()` and `.map()`:

```javascript
var select = $('#select');

var options = $.map(obj, function (value, key) {
    return '<option value="' + key + '">' + value + '</option>';
});

select.append(options);
```

##### Option 4:
Using `.append()` and `$.each()`:

```javascript
var select = $('#select');

$.each(obj, function (key, value) {
    select.append('<option value="' + key + '">' + value + '</option>');
});
```
