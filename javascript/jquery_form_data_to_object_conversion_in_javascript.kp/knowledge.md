---
title: Transform form data into a JavaScript object using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery`s .serializeArray() can be used to convert form data to a JavaScript object.
---

**Contents**

[TOC]

#### Section 1: Create Form

Create a form element with an id of `form` and add two input elements with their respective names and values.

```html
<form id="form">
    <input type="text" name="name" value="John Doe" />
    <input type="text" name="age" value="30" />
</form>
```

#### Section 2: Get Form Data

Use jQuery's `serializeArray()` method to get an array of objects containing the form data.

```js
var formData = $('#form').serializeArray();
```

#### Section 3: Convert to Object

Use `reduce()` to convert the array of objects into a single JavaScript object.

```js
var dataObj = formData.reduce(function(obj, item) {
    obj[item.name] = item.value;
    return obj;
}, {});
```

#### Section 4: Result

The resulting object will look like this:

```js
{
    name: "John Doe",
    age: "30"
}
```
