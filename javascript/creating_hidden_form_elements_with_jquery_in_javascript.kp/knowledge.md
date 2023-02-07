---
title: Generate a hidden form element dynamically using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery can create a hidden form element on the fly using the $(`<input type=`hidden`>`) syntax.
---

**Contents**

[TOC]

**Section 1 - Create a Form Element**

To create a hidden form element on the fly in Javascript, you can use the jQuery `.append()` method. This method allows you to add new elements to the end of an existing element. 

For example, the following code will create a new hidden form element with the attribute `name="test"` and the value `"testvalue"`:

```javascript
$('form').append('<input type="hidden" name="test" value="testvalue" />');
```

**Section 2 - Set the Value of the Element**

You can use the jQuery `.val()` method to set the value of the element. This method takes a single argument, which is the value you want to set the element to.

For example, the following code will set the value of the hidden form element `name="test"` to `"newvalue"`:

```javascript
$('input[name="test"]').val('newvalue');
```

**Section 3 - Retrieve the Value of the Element**

You can use the jQuery `.val()` method to retrieve the value of the element. This method does not take any arguments and will return the value of the element.

For example, the following code will retrieve the value of the hidden form element `name="test"`:

```javascript
var value = $('input[name="test"]').val();
```

**Section 4 - Remove the Element**

You can use the jQuery `.remove()` method to remove the element from the DOM. This method does not take any arguments and will remove the element from the DOM.

For example, the following code will remove the hidden form element `name="test"` from the DOM:

```javascript
$('input[name="test"]').remove();
```
