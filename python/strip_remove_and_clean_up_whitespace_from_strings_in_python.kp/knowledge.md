---
title: What is the method for removing all spaces from a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the replace() method with an empty string argument to remove all whitespace from a string in Python.
---

**Contents**

[TOC]

## Using replace() method

One way to strip all whitespace from a string in Python is by using the `replace()` method. This method substitutes a given character or sub-string with another one. In this case, we will substitute all whitespace characters `" "` with an empty string `""`.

```python
string_with_spaces = "  This is a string with spaces.  "
string_without_spaces = string_with_spaces.replace(" ", "")
```

In this code snippet, `string_with_spaces` is the input string that contains whitespace characters. The `replace()` method takes two arguments: the first one is the character or substring to be replaced, and the second one is the replacement character or substring. In this case, we replace `" "` with `""` to remove all white spaces.

The output string `string_without_spaces` will contain the same characters as the input string, but without any whitespace.

## Using split() and join() methods

Another way to strip all whitespace from a string is by using the `split()` and `join()` methods. The `split()` method splits a string into a list of substrings based on a given delimiter. By default, the delimiter is whitespace characters. We can then join the resulting list using the `join()` method with an empty string as the separator, effectively removing all whitespace.

```python
string_with_spaces = "  This is a string with spaces.  "
string_without_spaces = "".join(string_with_spaces.split())
```

In this code snippet, we first split the input string `string_with_spaces` into a list of substrings using the `split()` method. The resulting list will contain every sequence of non-whitespace characters as substrings.

We then join the list using the `join()` method with an empty separator `""`. This will concatenate all substrings in the list into a single string, with no whitespace characters between them.

## Using regular expressions

The `re` module in Python provides support for regular expressions, which are powerful tools for pattern matching and text manipulation. We can use a regular expression to match all whitespace characters in a string and replace them with an empty string.

```python
import re

string_with_spaces = "  This is a string with spaces.  "
string_without_spaces = re.sub("\s+", "", string_with_spaces)
```

In this code snippet, we import the `re` module and use the `sub()` function to replace substrings that match a regular expression pattern. The pattern `"\s+"` matches one or more whitespace characters, including spaces, tabs, and newlines.

The `sub()` function takes three arguments: the regular expression pattern to match, the replacement string (in this case, an empty string), and the input string.

The output string `string_without_spaces` will be the same as the input string, but with all whitespace characters removed
