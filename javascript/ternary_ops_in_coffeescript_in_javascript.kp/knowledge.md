---
title: An operation using three operands in coffeescript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: In CoffeeScript, a ternary operation is written as an expression with a question mark (?) before the first expression, a colon () between the two expressions, and the second expression after the colon.
---

**Contents**

[TOC]

### Syntax

In CoffeeScript, a ternary operation is written as:

`condition ? true-value : false-value`

In Javascript, the same ternary operation is written as:

`condition ? true-value : false-value`

### Example

In CoffeeScript, a ternary operation might be written as:

`x > 10 ? 'big' : 'small'`

In Javascript, the same ternary operation would be written as:

`x > 10 ? 'big' : 'small'`

### Usage

The ternary operation can be used to quickly evaluate a condition and assign a value based on the result. For example, the following code will assign the value `'big'` to the variable `size` if `x` is greater than 10, and `'small'` if `x` is less than or equal to 10:

`let size = x > 10 ? 'big' : 'small';`

### Output

The output of the ternary operation will be the value assigned to the variable. In the example above, the output will be either `'big'` or `'small'`, depending on the value of `x`.
