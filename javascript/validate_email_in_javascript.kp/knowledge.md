---
title: What is the process for verifying an email address using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can validate an email address in JavaScript by using a regular expression to check if it matches the expected format.
---

**Contents**

[TOC]

### Using Regular Expressions

Regular expressions are a powerful tool for validating email addresses. The following is a basic regular expression for validating email addresses:

```
/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$/
```

To use this regular expression, you can use the `test()` method of the `RegExp` object:

```
let email = "example@example.com";
let regex = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?(?:\.[a-zA-Z0-9](?:[a-zA-Z0-9-]{0,61}[a-zA-Z0-9])?)*$/;

if (regex.test(email)) {
  console.log("Valid email address");
} else {
  console.log("Invalid email address");
}
```

### Using HTML5 Form Validation

HTML5 provides a built-in form validation API that can be used to validate email addresses. To use the HTML5 form validation API, you need to set the `type` attribute of the `input` element to `email`:

```
<input type="email" name="email" required>
```

When the form is submitted, the browser will automatically validate the email address. If the email address is invalid, the browser will display an error message.

### Using a Third-Party Library

There are several third-party libraries available for validating email addresses in JavaScript. For example, the [validator.js](https://github.com/validatorjs/validator.js) library provides an `isEmail()` function for validating email addresses:

```
let validator = require('validator');
let email = "example@example.com";

if (validator.isEmail(email)) {
  console.log("Valid email address");
} else {
  console.log("Invalid email address");
}
```
