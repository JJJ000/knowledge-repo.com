---
title: What is the best way to ensure that a decimal is always displayed with two decimal places?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the string formatting method `f` with a precision of 2 (e.g. `{.2f}`).
---

**Contents**

[TOC]

### Using the Format Function

The `format` function can be used to format a decimal to always show two decimal places.

```
#Format a decimal to always show two decimal places
x = 1.2345
print(format(x, '.2f'))

#Output: 1.23
```

### Using the Round Function

The `round` function can also be used to format a decimal to always show two decimal places.

```
#Format a decimal to always show two decimal places
x = 1.2345
print(round(x,2))

#Output: 1.23
```

### Using the F-String

The f-string can also be used to format a decimal to always show two decimal places.

```
#Format a decimal to always show two decimal places
x = 1.2345
print(f'{x:.2f}')

#Output: 1.23
```

### Using the Format Specification Mini-Language

The format specification mini-language can also be used to format a decimal to always show two decimal places.

```
#Format a decimal to always show two decimal places
x = 1.2345
print('{:.2f}'.format(x))

#Output: 1.23
```
