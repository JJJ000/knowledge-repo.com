---
title: What is the best way to take out a portion of a string from the end?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the string slicing syntax to create a substring from the beginning of the string to the index before the end of the substring you want to remove.
---

**Contents**

[TOC]

## 1. Using rstrip()

The `rstrip()` method can be used to remove a substring from the end of a string. It takes in the substring to be removed as an argument and returns a new string with the substring removed from the end.

Example:

```python
my_string = "This is a test string"

# Remove the substring "string" from the end of the string
my_string = my_string.rstrip("string")

print(my_string) # Output: This is a test
```

## 2. Using Slicing

Slicing can be used to remove a substring from the end of a string. The substring to be removed is specified in the slicing syntax.

Example:

```python
my_string = "This is a test string"

# Remove the substring "string" from the end of the string
my_string = my_string[:-6]

print(my_string) # Output: This is a test
```

## 3. Using replace()

The `replace()` method can also be used to remove a substring from the end of a string. It takes in the substring to be removed as the first argument and an empty string as the second argument.

Example:

```python
my_string = "This is a test string"

# Remove the substring "string" from the end of the string
my_string = my_string.replace("string", "")

print(my_string) # Output: This is a test
```

## 4. Using split()

The `split()` method can also be used to remove a substring from the end of a string. It takes in the substring to be removed as an argument and returns a list of strings after splitting the string. The last item in the list is the string with the substring removed from the end.

Example:

```python
my_string = "This is a test string"

# Remove the substring "string" from the end of the string
my_string_list = my_string.split("string")
my_string = my_string_list[0]

print(my_string) # Output: This is a test
```
