---
title: How can we eliminate all non-numeric characters in a Python string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use regular expressions and the re module in Python to remove all non-numeric characters from a string using the following code re.sub(r`\D`, ``, string).
---

**Contents**

[TOC]

# Method 1: Using isdigit() method

One way to remove all non-numeric characters from a string in Python is to iterate through each character in the string and check if it is a digit using the `isdigit()` method. If the character is a digit, we append it to a new string, otherwise we skip it. Here's the code:

```python
def remove_non_numeric_chars(input_str):
    """
    Removes all non-numeric characters from a string
    """
    result_str = ''
    for char in input_str:
        if char.isdigit():
            result_str += char
    return result_str
```
Example Usage:

```python
>>> input_str = 'abc123def456'
>>> remove_non_numeric_chars(input_str)
'123456'
```

# Method 2: Using regular expressions

Another way to remove all non-numeric characters from a string in Python is to use regular expressions. We can use the `re` module and the `sub()` function to replace all non-numeric characters with an empty string. Here's the code:

```python
import re

def remove_non_numeric_chars(input_str):
    """
    Removes all non-numeric characters from a string using regular expressions
    """
    return re.sub('[^0-9]', '', input_str)
```

Example Usage:

```python
>>> input_str = 'abc123def456'
>>> remove_non_numeric_chars(input_str)
'123456'
```

# Method 3: Using filter() function

We can also use the built-in filter() function with isdigit() inside a lambda function to remove all non-numeric characters from a string. Here is the code:

```python
def remove_non_numeric_chars(input_str):
    """
    Removes all non-numeric characters from a string using the filter() function
    """
    return ''.join(filter(lambda x: x.isdigit(), input_str))
```

Example Usage:

```python
>>> input_str = 'abc123def456'
>>> remove_non_numeric_chars(input_str)
'123456'
```

All three methods above will return '123456' when applied to the input string 'abc123def456'.
