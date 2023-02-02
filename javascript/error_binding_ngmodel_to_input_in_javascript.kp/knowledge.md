---
title: The 'input' element does not have a known property called 'ngmodel', so it cannot be bound to
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The ngModel directive is not available for use with plain JavaScript, it must be used with an Angular application.
---

**Contents**

[TOC]

## What is ngModel?

ngModel is a directive in Angular.js that creates a two-way data binding between the view and the model. It allows the user to interact with the application by changing the values in the view and having those changes reflected in the model and vice versa.

## Why Can't We Bind to ngModel?

ngModel is not a known property of the HTML input element in JavaScript, so it cannot be bound to it. The ngModel directive is a feature of Angular.js, which is a JavaScript framework, and is not part of the standard HTML specification. 

## What is the Alternative?

The alternative to binding to ngModel is to use the standard HTML form elements and their associated events. This means that the data binding must be done manually by listening for events such as change, input, and blur. The data can then be processed and the model updated accordingly.

## How to Implement the Alternative?

To implement the alternative, you must first create an event listener for the form element. This can be done using the addEventListener() method. Then, you must define a function to handle the event and update the model accordingly. Finally, you must call the event listener on the form element. This process can be repeated for each form element that needs to be bound to the model.
