---
title: What is the best way to remove whitespace from a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the string method strip() to trim whitespace from a string in Python.
---

**Contents**

[TOC]

### Using the strip() Method

The strip() method can be used to remove whitespace from the beginning and end of a string.

```
my_string = "   Hello World     "

my_string.strip()  # returns "Hello World"
```

### Using the replace() Method

The replace() method can be used to replace all occurrences of a substring with another substring. This can be used to replace all whitespace with an empty string.

```
my_string = "   Hello World     "

my_string.replace(" ", "")  # returns "HelloWorld"
```

### Using Regular Expressions

The re module provides regular expression matching operations. The sub() method can be used to replace all occurrences of a pattern with a replacement string.

```
import re

my_string = "   Hello World     "

re.sub("\s+", "", my_string)  # returns "HelloWorld"
```

### Using the join() Method

The join() method can be used to join a list of strings using a separator string. This can be used to remove whitespace from the beginning and end of a string.

```
my_string = "   Hello World     "

"".join(my_string.split())  # returns "HelloWorld"
```
