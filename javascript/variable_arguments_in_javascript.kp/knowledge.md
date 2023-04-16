---
title: A JavaScript function that accepts a variable amount of arguments
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JavaScript, functions can accept a variable number of arguments by using the `arguments` object.
---

**Contents**

[TOC]

## Using the Arguments Object

The `arguments` object is an array-like object accessible inside functions that contains the values of the arguments passed to that function. It can be used to access arguments passed to a function when the number of arguments is not known or can vary.

## Using the Rest Operator

The rest operator (`...`) is a way to capture an indefinite number of arguments into an array. It can be used in place of the traditional `arguments` object to access an indefinite number of arguments passed to a function.

## Using the Spread Operator

The spread operator (`...`) is a way to expand an array into its individual elements. It can be used to pass an array of arguments to a function.

## Using the apply() Method

The `apply()` method allows us to call a function with an array of arguments. This is useful when we have an array of arguments that we want to pass to a function.
