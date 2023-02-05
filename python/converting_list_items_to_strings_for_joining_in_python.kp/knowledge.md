---
title: What is the best way to convert each item in the list to a string so that I can join them together?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str() function to convert each item in the list to a string.
---

**Contents**

[TOC]

### Using `str()`

The `str()` function can be used to convert each item in a list to a string.

```python
# Sample list
my_list = [1, 2, 3]

# Converting each item to a string
my_list_str = [str(item) for item in my_list]

# Print the new list
print(my_list_str)
# Output: ['1', '2', '3']
```

### Using `join()`

The `join()` function can be used to join a list of strings together.

```python
# Sample list
my_list = ['1', '2', '3']

# Joining the list
my_string = ''.join(my_list)

# Print the string
print(my_string)
# Output: 123
```

### Combining `str()` and `join()`

The `str()` and `join()` functions can be combined to convert each item in a list to a string, and then join them together.

```python
# Sample list
my_list = [1, 2, 3]

# Converting each item to a string and joining the list
my_string = ''.join(str(item) for item in my_list)

# Print the string
print(my_string)
# Output: 123
```
