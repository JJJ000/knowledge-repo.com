---
title: What is the syntax for rounding a number to two decimal places in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in round() function and specify the number of decimal places to round to (in this case, 2).
---

**Contents**

[TOC]

### Using the Round Function

The `round()` function can be used to round a number to a specified number of decimal places. The syntax for this function is `round(number, ndigits)`, where `number` is the number to be rounded and `ndigits` is the number of decimal places to round to.

For example, to round the number 3.14159 to two decimal places, the following code can be used:

```
rounded_number = round(3.14159, 2)
```

The value of `rounded_number` will be `3.14`.

### Using String Formatting

Another way to round a number to two decimal places is to use the string formatting method. This method works by converting the number to a string, and then specifying the number of decimal places to display.

The syntax for this method is `'{:.nf}'.format(number)`, where `n` is the number of decimal places to display and `number` is the number to be rounded.

For example, to round the number 3.14159 to two decimal places, the following code can be used:

```
rounded_number = '{:.2f}'.format(3.14159)
```

The value of `rounded_number` will be `3.14`.
