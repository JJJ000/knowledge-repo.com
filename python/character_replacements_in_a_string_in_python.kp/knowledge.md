---
title: Substituting occurrences of a character within a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To replace instances of a character in a string in Python, use the replace() method.
---

**Contents**

[TOC]

Section 1: Introduction

Python provides several ways to manipulate strings, and one of the most common tasks is to replace instances of a character within a string. In this article, we will explore three different methods for replacing instances of a character in a string in Python. These three methods are:

1. Using the replace() method
2. Using the translate() method
3. Using a regular expression


Section 2: Using the replace() method

The replace() method is a built-in method of the Python string class that allows you to replace all instances of a particular character within a string. The syntax of the method is as follows:

```
string.replace(old, new, max)
```

Where:

* `string` is the original string
* `old` is the character to be replaced
* `new` is the character to replace the old one
* `max` (optional) is the maximum number of replacements to perform. If not specified, all instances of the old character will be replaced.

Here's an example of how to use the replace() method to replace all instances of the letter "a" with the letter "b" within a string:

```python
original_string = "abcdeabeeebca"
new_string = original_string.replace("a", "b")
print(new_string)
```

This will output: "bbcdebbeeebcb"


Section 3: Using the translate() method

The translate() method is another built-in method of the Python string class that can be used to replace instances of a character within a string. The syntax of the method is as follows:

```
string.translate(table)
```

Where:

* `string` is the original string
* `table` is a translation table. This table can be created using the maketrans() method of the string class.

Here's an example of how to use the translate() method to replace all instances of the letter "a" with the letter "b" within a string:

```python
original_string = "abcdeabeeebca"
translation_table = str.maketrans("a", "b")
new_string = original_string.translate(translation_table)
print(new_string)
```

This will output: "bbcdebbeeebcb"


Section 4: Using a regular expression

Finally, you can use regular expressions to replace instances of a character within a string. Regular expressions provide a powerful and flexible way to match and manipulate strings. In Python, regular expressions are implemented using the re module. Here's an example of how to use regular expressions to replace all instances of the letter "a" with the letter "b" within a string:

```python
import re

original_string = "abcdeabeeebca"
new_string = re.sub('a', 'b', original_string)
print(new_string)
```

This will output: "bbcdebbeeebcb"
