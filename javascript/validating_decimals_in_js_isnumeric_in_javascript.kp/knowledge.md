---
title: Check if a number is a valid decimal in JavaScript using the isnumeric() function
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Yes, the IsNumeric() function in Javascript can be used to validate decimal numbers.
---

**Contents**

[TOC]

## Overview
The IsNumeric() function in Javascript is used to validate if a given value is a valid decimal number. It is a built-in function of the JavaScript language and can be used to check if a given value is a valid number or not.

## Syntax
The syntax of the IsNumeric() function is as follows:

```
isNumeric(value)
```

where `value` is the value to validate.

## Examples
Here are some examples of using the IsNumeric() function:

```
isNumeric("10.5") // returns true
isNumeric("abc") // returns false
isNumeric("1.2.3") // returns false
isNumeric("-10") // returns true
```

## Return Value
The IsNumeric() function returns a Boolean value of `true` if the given value is a valid decimal number and `false` if it is not.
