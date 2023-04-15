---
title: What is the best way to add spaces to a Python string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the string method `.rjust()` to add spaces to a string.
---

**Contents**

[TOC]

### Using the `str.center()` Method

The `str.center()` method allows you to fill out a Python string with spaces. It takes two parameters: the length of the desired string and the character used to fill in the spaces (defaults to a space character).

For example:

```python
my_string = "Hello World"

# Fill out the string with 10 spaces
new_string = my_string.center(10)

print(new_string)
```

The above code will output: `"  Hello World  "`

### Using the `str.ljust()` and `str.rjust()` Methods

The `str.ljust()` and `str.rjust()` methods also allow you to fill out a Python string with spaces. They take two parameters: the length of the desired string and the character used to fill in the spaces (defaults to a space character).

The `str.ljust()` method will add spaces to the right side of the string, while the `str.rjust()` method will add spaces to the left side of the string.

For example:

```python
my_string = "Hello World"

# Fill out the string with 10 spaces on the left side
new_string = my_string.ljust(10)

print(new_string)
```

The above code will output: `"Hello World  "`

### Using the `str.zfill()` Method

The `str.zfill()` method allows you to fill out a Python string with zeroes. It takes one parameter: the length of the desired string.

For example:

```python
my_string = "Hello World"

# Fill out the string with 10 zeroes
new_string = my_string.zfill(10)

print(new_string)
```

The above code will output: `"000Hello World"`
