---
title: How do the JSON and simplejson Python modules differ?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The simplejson module is a faster and more feature-rich alternative to the JSON module.
---

**Contents**

[TOC]

### Syntax
The syntax of the two modules is largely the same. The main difference is that simplejson allows a few extra parameters that json does not. For example, simplejson allows one to specify an indentation level when encoding data. 

### Performance
The performance of simplejson is generally better than json. This is because simplejson is written in C, while json is written in Python.

### Error Handling
In terms of error handling, simplejson is more robust than json. It is able to detect and handle errors more effectively.

### Compatibility
simplejson is more compatible with newer versions of Python than json. For example, simplejson is compatible with Python 3, while json is not.
