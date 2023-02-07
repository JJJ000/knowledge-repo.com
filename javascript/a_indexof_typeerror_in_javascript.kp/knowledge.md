---
title: An error occurred when opening a new foundation project "uncaught typeerror - a.indexof is not a function"
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: This error occurs when attempting to use the indexOf method on a variable that is not an array or a string.
---

**Contents**

[TOC]

## Description
The "Uncaught TypeError: a.indexOf is not a function" error is an error that occurs when attempting to use the `indexOf` method on an object that does not have the `indexOf` method. This error typically occurs when attempting to use the `indexOf` method on an array or string.

## Causes
This error can occur for a few different reasons. It can occur when attempting to use the `indexOf` method on an object that does not have the `indexOf` method, such as a number or boolean. It can also occur when attempting to use the `indexOf` method on an array or string with an invalid argument. For example, if the argument is not a string or number, the `indexOf` method will throw an error.

## Solutions
The solution to this error depends on the cause. If the error is occurring because the `indexOf` method is being used on an object that does not have the `indexOf` method, then the code should be changed to use a different method that is appropriate for the object. If the error is occurring because the `indexOf` method is being used on an array or string with an invalid argument, then the argument should be changed to a valid string or number.
