---
title: How can a Python integer be converted to a binary string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the bin() function to convert an int to a binary string.
---

**Contents**

[TOC]

# Section 1: Convert Integer to Binary

The first step is to convert the given integer to a binary number. This can be done by using the `bin()` function.

```
binary_string = bin(integer)
```

# Section 2: Remove Prefix

The `bin()` function prefixes the binary string with `0b`. To remove this prefix, we can use the `slice()` method.

```
binary_string = binary_string[2:]
```

# Section 3: Format Output

The output of the `bin()` function is a string of 0s and 1s. To format the output, we can use the `format()` function.

```
binary_string = format(binary_string, '0>8')
```

This will pad the string with 0s until it has 8 characters.

# Section 4: Final Output

Once the integer has been converted to a binary string, and the output is formatted, the final output is ready.

```
print(binary_string)
```
