---
title: Eliminate the initial character from a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can remove the first character of a string in Python by using string slicing, like this new\_string = original\_string[1].
---

**Contents**

[TOC]

## Method 1: String slicing

One of the easiest ways to remove the first character of a string in Python is by using string slicing. This method involves creating a new string that starts from the second character of the original string and goes up to the end.

```python
s = "Hello World!"
s = s[1:]
print(s)
```

Output:
```
ello World!
```

In the example above, the original string `s` is sliced from the index 1 (which corresponds to the second character 'e') up to the end using the colon `:` operator. The resulting string is then assigned back to `s` variable.


## Method 2: Using string manipulation functions

Python provides a variety of string manipulation functions that can be used to perform various operations on strings, including removing characters at the beginning or end of a string. One such function is the `lstrip()` method, which removes leading whitespaces or specified characters from the left side of a string.

```python
s = "    Hello World!"
s = s.lstrip()
print(s)
```

Output:
```
Hello World!
```

In the example above, the `lstrip()` method is used to remove any leading whitespaces from the beginning of the string `s`.


## Method 3: Converting string to a list and joining back

Another way to remove the first character of a string is to convert the string to a list, remove the first element of the list, and then join it back to a string using the `join()` method.

```python
s = "Hello World!"
s = ''.join(list(s)[1:])
print(s)
```

Output:
```
ello World!
```

In the example above, the string `s` is first converted to a list using the `list()` function. The first element of the list (which corresponds to the first character of the original string) is then removed using slicing. Finally, the remaining elements of the list are joined back to form a new string, which is assigned back to `s`.
