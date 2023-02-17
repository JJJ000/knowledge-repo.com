---
title: Javascript large number
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Javascript long integers in JSON must be stored as strings.
---

**Contents**

[TOC]

# Overview

Javascript long integers are numbers that are too large for the regular Javascript number type to store. These numbers are represented in JSON as strings, and must be converted back to a number for use in Javascript.

# Representation

Javascript long integers are represented in JSON as strings. The string must be a valid number in order for the JSON parser to recognize it. This means that the string must have no leading or trailing whitespace, and must have a valid number format (e.g. -1234567890).

# Conversion

Once the string is parsed, it must be converted back to a number in order to be used in Javascript. This can be done using the Javascript built-in function `parseInt()` or `parseFloat()`, depending on the type of number.

# Limitations

The main limitation of using JSON to represent Javascript long integers is that the number must be represented as a string. This means that the number cannot be used directly without conversion, and any operations performed on the number must be done using the appropriate functions.
