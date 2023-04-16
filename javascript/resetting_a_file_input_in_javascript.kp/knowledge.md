---
title: What is the process for resetting an <input type="file">?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `value` property to set the value of the file input to an empty string.
---

**Contents**

[TOC]

1. Using `value` Property #

The `value` property of the `<input type="file">` element can be used to reset the file input.

```javascript
document.getElementById("myFile").value = "";
```

2. Using `createElement` and `cloneNode` #

The `createElement` and `cloneNode` methods can be used to reset the file input.

```javascript
var fileInput = document.getElementById("myFile");
var newInput = document.createElement("input");
newInput.type = "file";
fileInput.parentNode.replaceChild(newInput, fileInput);
```

3. Using `form.reset` #

The `form.reset` method can also be used to reset the file input.

```javascript
var form = document.getElementById("myForm");
form.reset();
```

4. Using `jQuery` #

The `val` method of jQuery can also be used to reset the file input.

```javascript
$("#myFile").val("");
```
