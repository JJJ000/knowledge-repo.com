---
title: Take away the last letter from the string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: String[-1] will remove the final character from the string.
---

**Contents**

[TOC]

### Using Slicing

We can use slicing to remove the last character from a string in Python. To do this, we use the following syntax:

```python
string[:-1]
```

This will return a new string with the last character removed.

### Using rstrip()

We can also use the `rstrip()` function to remove the last character from a string in Python. This function removes any trailing whitespace from the end of the string. To use this function, we use the following syntax:

```python
string.rstrip()
```

This will return a new string with the last character removed.

### Using replace()

We can also use the `replace()` function to remove the last character from a string in Python. This function replaces any specified character with another character. To use this function, we use the following syntax:

```python
string.replace(old_char, '')
```

This will return a new string with the last character removed.

### Using pop()

Finally, we can use the `pop()` function to remove the last character from a string in Python. This function removes the last element from a list. To use this function, we use the following syntax:

```python
string_list = list(string)
string_list.pop()
string = ''.join(string_list)
```

This will return a new string with the last character removed.
