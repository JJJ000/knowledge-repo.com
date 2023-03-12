---
title: Divide a string using newline character as a separator in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the split() method with `\n` as the delimiter to split a string using a newline in Python.
---

**Contents**

[TOC]

## Introduction
Splitting a string using a newline delimiter is a common task in Python. This can be done easily using the built-in `split()` method. In this article, we will discuss the different methods of splitting a string in Python using a newline delimiter. 

## Method 1: Using split() method
The `split()` method can be used to split a string using any delimiter. In this case, we will use the newline delimiter "\n" to split the string.

```python
string = "Hello\nWorld\n!"
string_list = string.split("\n")
print(string_list)
```
Output:
```
["Hello", "World", "!"]
```

## Method 2: Using rsplit() method
Like `split()`, the `rsplit()` method can be used to split a string using any delimiter. The only difference is that it starts splitting the string from the right side.

```python
string = "Hello\nWorld\n!"
string_list = string.rsplit("\n")
print(string_list)
```
Output:
```
["Hello", "World", "!"]
```

## Method 3: Using re.split() method
The `re.split()` method can be used to split a string using a regular expression pattern. In this case, we will use the newline character "\n" as the pattern.

```python
import re

string = "Hello\nWorld\n!"
string_list = re.split("\n", string)
print(string_list)
```
Output:
```
["Hello", "World", "!"]
```

## Conclusion
In this article, we discussed three different methods of splitting a string using a newline delimiter in Python. All three methods are simple and easy to use.
