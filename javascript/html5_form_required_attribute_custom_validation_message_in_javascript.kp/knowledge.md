---
title: What is the html5 required attribute for a form, and how can I set a custom validation message?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The custom validation message for an HTML5 form required attribute can be set using the setCustomValidity() method in Javascript.
---

**Contents**

[TOC]

#### Setting the Attribute

The required attribute can be set on an HTML5 form element by adding the attribute to the element like this:

```html
<input type="text" required>
```

#### Setting the Custom Validation Message

The custom validation message can be set using Javascript by accessing the element and setting the `setCustomValidity()` method:

```javascript
document.getElementById("myInput").setCustomValidity("Please enter a valid value");
```

#### Triggering the Validation Message

The validation message will be triggered when an invalid value is entered into the field and the form is submitted.

#### Resetting the Validation Message

To reset the validation message, the `setCustomValidity()` method can be called with an empty string:

```javascript
document.getElementById("myInput").setCustomValidity("");
```
