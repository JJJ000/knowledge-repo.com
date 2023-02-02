---
title: Turn a list of characters into a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The list of characters can be converted into a string by using the ``.join(list) method.
---

**Contents**

[TOC]

### Using `join`

The `join` method can be used to join a list of characters into a string. The syntax is `separator.join(iterable)`, where `separator` is the string used to join the characters and `iterable` is the list of characters.

For example:

```python
characters = ['a', 'b', 'c', 'd']

string = ''.join(characters)
print(string) # abcd
```

### Using `str.join`

The `str.join` method is a more concise way of joining a list of characters into a string. The syntax is `iterable.join(string)`, where `iterable` is the list of characters and `string` is the string used to join the characters.

For example:

```python
characters = ['a', 'b', 'c', 'd']

string = ''.join(characters)
print(string) # abcd
```

### Using a `for` loop

A `for` loop can be used to iterate through a list of characters and concatenate each character onto a string.

For example:

```python
characters = ['a', 'b', 'c', 'd']

string = ''
for char in characters:
    string += char

print(string) # abcd
```
