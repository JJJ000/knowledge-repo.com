---
title: How to transform form information into a Javascript object using jQuery
authors:
- cool_wizard
tags:
- javascript
- jquery
- json
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-15 00:00:00
updated_at: 2023-01-15 00:00:00
tldr: jQuery's `.serializeArray()` method can be used to convert form data to a JavaScript object in JSON format.
---

**Contents**

[TOC]

### Create a Form

The first step in converting form data to a JavaScript object with jQuery is to create a form. The form should include input fields for the data that you wish to convert. The form could also have a submit button to allow the user to submit the form data.

### Create a JavaScript Object

The next step is to create a JavaScript object to store the form data. This can be done with the following code:

```javascript
var formData = {};
```

### Retrieve Form Data

Once the object is created, the form data can be retrieved using jQuery. The following code can be used to retrieve the form data:

```javascript
$('form').each(function(){
  $(this).find('input').each(function(){
    formData[$(this).attr('name')] = $(this).val();
  });
});
```

### Convert to JSON

Finally, the form data can be converted to JSON using the following code:

```javascript
var jsonData = JSON.stringify(formData);
```
