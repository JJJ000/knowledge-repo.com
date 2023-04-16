---
title: Using jquery to reset the value of an input element of type 'file'
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: $(`input[type=`file`]`).val(``);
---

**Contents**

[TOC]

1. Selecting the File Input Element
----------------------------------
Using jQuery, you can select the file input element by using the following code:

```javascript
var fileInput = $('input[type="file"]');
```

2. Clearing the File Input
--------------------------
Once you have the file input element, you can clear its value by setting it to an empty string:

```javascript
fileInput.val('');
```

3. Resetting the File Input
---------------------------
You can also reset the file input to its initial state by using the jQuery `reset()` method:

```javascript
fileInput.reset();
```

4. Resetting the Form
---------------------
If the file input is part of a form, you can reset the entire form to its initial state by using the jQuery `resetForm()` method:

```javascript
$('form').resetForm();
```
