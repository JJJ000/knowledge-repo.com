---
title: What is the method to eliminate zeros at the beginning and end of a string in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the strip() method with `0` as argument to remove leading and trailing zeros from the string in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In some cases, we may want to remove the leading and trailing zeros in a string. For example, if we are working with financial data, we may want to remove the trailing zeros to make the output more readable. In this article, we will discuss different ways to remove leading and trailing zeros from a string in Python.

Section 2: Using the strip() method
We can use the strip() method to remove leading and trailing zeros from a string. By default, the strip() method removes all whitespace characters from the beginning and end of a string. However, we can pass a string argument to the method to specify the characters that we want to remove. Here's an example:

```
text = '0000123.000'
new_text = text.strip('0')
print(new_text)
```

Output:
```
123.
```

As we can see, the strip() method removed all leading and trailing zeros from the string.

Section 3: Using the lstrip() and rstrip() methods
Alternatively, we can use the lstrip() and rstrip() methods to remove leading and trailing zeros in a string respectively. The lstrip() method removes leading characters from a string, while the rstrip() method removes trailing characters. Here's an example:

```
text = '0000123.000'
new_text = text.lstrip('0').rstrip('0')
print(new_text)
```

Output:
```
123.
```

As we can see, the lstrip() method removed the leading zeros, while the rstrip() method removed the trailing zeros.

Section 4: Using regular expressions
We can also use regular expressions to remove leading and trailing zeros from a string. The re.sub() function can be used to replace a pattern in a string with a new pattern. We can define a regular expression pattern to match all leading and trailing zeros in a string and replace them with an empty string. Here's an example:

```
import re

text = '0000123.000'
pattern = '^0+|0+$'
new_text = re.sub(pattern, '', text)
print(new_text)
```

Output:
```
123.
```

The "^0+" in the pattern matches all leading zeros, while "0+$" matches all trailing zeros. The re.sub() function replaces the matched pattern with an empty string, effectively removing the leading and trailing zeros.
