---
title: Calling a function without parentheses
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In Javascript, invoking a function without parentheses is not possible.
---

**Contents**

[TOC]

# Invoking a Function Without Parentheses

In JavaScript, functions can be invoked without parentheses in certain scenarios. This is known as a Function Invocation Pattern.

## Syntax

The syntax for invoking a function without parentheses is as follows:

```
functionName argument1, argument2, ...
```

## Examples

Here are some examples of invoking a function without parentheses:

```
// Invoking a function with one argument
functionName argument1

// Invoking a function with multiple arguments
functionName argument1, argument2, argument3
```

## Limitations

It is important to note that this pattern is not supported in all JavaScript environments and should not be used in production code. Additionally, this pattern only works with functions that accept a single argument or multiple arguments separated by commas.
