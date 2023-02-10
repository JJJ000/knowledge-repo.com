---
title: Generating a JSON object dynamically based on each input value using jquery
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The jQuery .each() function can be used to iterate through each input value and dynamically build a JSON object.
---

**Contents**

[TOC]

## Section 1: HTML Markup

The HTML markup should include a form with input elements.

```html
<form id="myForm">
  <input type="text" name="name" placeholder="Name">
  <input type="text" name="address" placeholder="Address">
  <input type="text" name="phone" placeholder="Phone">
  <input type="submit" value="Submit">
</form>
```

## Section 2: jQuery

The jQuery code should include a function to capture the form input values and create a JSON object.

```javascript
$("#myForm").submit(function(e){
  e.preventDefault();

  var formData = $(this).serializeArray();
  var jsonData = {};

  $(formData).each(function(i, field){
    jsonData[field.name] = field.value;
  });

  console.log(jsonData);
});
```

## Section 3: Output

The output should be a JSON object containing the form input values.

```json
{
  "name": "John Doe",
  "address": "123 Main St.",
  "phone": "123-456-7890"
}
```

## Section 4: Usage

The JSON object can be used to store the form input values in a database or send to an API.
