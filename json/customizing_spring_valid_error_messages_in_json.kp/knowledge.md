---
title: What is the process for altering the standard error message associated with spring @valid validation?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can customize the default error message from spring @Valid validation by using the @Message annotation.
---

**Contents**

[TOC]

1. Create a Custom ConstraintValidator 

Create a custom ConstraintValidator for the @Valid annotation. The ConstraintValidator will be responsible for validating the constraints and setting the custom error message.

2. Override the Default Error Message 

Override the default error message in the ConstraintValidator by implementing the isValid() method. Inside the method, use the ConstraintValidatorContext to set the custom error message.

3. Add the Custom Error Message to the Response

Add the custom error message to the response by implementing an ErrorHandler. The ErrorHandler will be responsible for setting the custom error message in the response.

4. Configure the ErrorHandler

Configure the ErrorHandler in the application context file. This will enable the ErrorHandler to be called when a validation error occurs.
