---
title: Why does (0 < 5 and 5 < 3) return true?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The expression is evaluated as (0 < 5) && (5 < 3), which is true because the first part is true.
---

**Contents**

[TOC]

### Explanation
The expression `(0 < 5 < 3)` is evaluated using the associativity of the less-than operator. First, the expression `0 < 5` is evaluated to be true. Then, the expression `true < 3` is evaluated, which is also true. Therefore, the expression `(0 < 5 < 3)` overall evaluates to true.

### Associativity
The less-than operator `<` is left-associative. This means that when multiple less-than operators are used in a row, the expression is evaluated from left to right.

### Example
For example, `(1 < 2 < 3)` is evaluated by first comparing `1 < 2` to be true. Then, the expression `true < 3` is evaluated, which is also true. Therefore, the expression `(1 < 2 < 3)` evaluates to true.

### Summary
In summary, the expression `(0 < 5 < 3)` evaluates to true because of the left-associativity of the less-than operator. The expression is evaluated from left to right, first comparing `0 < 5` to be true and then comparing `true < 3` to be true.
