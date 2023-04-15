---
title: What are the distinctions between using the call and apply methods?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Call invokes a function with a given this value and arguments provided individually, while apply invokes a function with a given this value and arguments provided as an array.
---

**Contents**

[TOC]

### Syntax

The syntax for call and apply are similar, but differ in how the arguments are passed.

Call: 
`func.call(thisArg, arg1, arg2, ...)`

Apply: 
`func.apply(thisArg, [argsArray])`

### Arguments

The main difference between call and apply is the way arguments are passed. Call requires the arguments to be passed in separately, while apply requires the arguments to be passed in as an array.

### Usage

Call is typically used when the number of arguments are known, while apply is used when the number of arguments are unknown or variable.

### Context

The other key difference between call and apply is the context in which the function is executed. The context is defined by the first argument passed to call and apply. When using call, the context is explicitly set. When using apply, the context is set to the array passed as the second argument.
