---
title: Show numbers with preceding zeroes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the format() method with a `0` flag to display a number with leading zeros.
---

**Contents**

[TOC]

# Using Format

The easiest way to print a number with leading zeros is to use the `format` function.

```python
number = 5
print("{:03d}".format(number))
```

The `:03d` part of the format string tells Python to render the number with 3 digits, padding the number with zeros on the left.

# Using Zfill

Another way to print a number with leading zeros is to use the `zfill` method.

```python
number = 5
print(str(number).zfill(3))
```

The `zfill` method adds leading zeros to the number until the total length of the string is equal to the argument passed to the method.

# Using F-Strings

You can also use f-strings to print a number with leading zeros.

```python
number = 5
print(f"{number:03d}")
```

The `:03d` part of the format string tells Python to render the number with 3 digits, padding the number with zeros on the left.

# Using String Formatting

Finally, you can also use string formatting to print a number with leading zeros.

```python
number = 5
print("%03d" % number)
```

The `%03d` part of the format string tells Python to render the number with 3 digits, padding the number with zeros on the left.
