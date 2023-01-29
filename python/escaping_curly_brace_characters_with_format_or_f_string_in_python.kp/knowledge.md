---
title: What is the best way to include curly-brace ({}) characters in a string when using .format (or an f-string)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use double curly-braces ({{}}) to escape curly-braces in a string while using .format or an f-string.
---

**Contents**

[TOC]

**Using .format()**

1. Brace Notation:
    Brace notation can be used to escape curly braces in a string while using the .format() method. This is done by adding an additional set of braces around the brace character to be escaped. For example, `'{{}}'.format(x)` will print `{}` where `x` is the value of the argument passed to the .format() method.

2. Percent Notation:
    Percent notation can also be used to escape curly braces in a string while using the .format() method. This is done by adding an additional percent sign before the brace character to be escaped. For example, `'%{}'.format(x)` will print `{}` where `x` is the value of the argument passed to the .format() method.

**Using f-string**

1. Brace Notation:
    Brace notation can also be used to escape curly braces in a string while using an f-string. This is done by adding an additional set of braces around the brace character to be escaped. For example, `f'{{}}'` will print `{}`.

2. Backslash Notation:
    Backslash notation can also be used to escape curly braces in a string while using an f-string. This is done by adding a backslash before the brace character to be escaped. For example, `f'\{}'` will print `{}`.
