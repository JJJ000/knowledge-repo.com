---
title: What is the process for creating a custom rule using the jquery validate plugin?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Create a custom validation method using the jQuery.validator.addMethod() function.
---

**Contents**

[TOC]

1. Create a Custom Rule Function
-------------------------
The jQuery Validate Plugin allows you to create custom rules by defining a rule function. This function should accept three parameters:

- The value of the element being validated
- The elements being validated
- An options object that contains any additional parameters

The function should return true if the value is valid, or false if it is not.

2. Add the Rule to the Plugin
-------------------------
Once the rule function has been created, it must be added to the jQuery Validate Plugin. This can be done by calling the addMethod method on the jQuery.validator object.

The addMethod method takes two parameters:

- The name of the rule
- The rule function

3. Use the Rule in a Form
-------------------------
The custom rule can then be used in a form by adding an attribute to the input element. The attribute should be named after the rule and should contain any additional parameters that are needed by the rule function.

For example, if the rule is named “myrule”, then the attribute should be named “data-rule-myrule”.

4. Test the Rule
-------------------------
Once the rule has been added to the form, it should be tested to make sure that it is working as expected. This can be done by submitting the form and verifying that the validation messages are displayed as expected.
