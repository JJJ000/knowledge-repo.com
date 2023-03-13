---
title: The re module of Python checks if a string matches a given regex pattern and returns true if a match is found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The re.search() function in Python`s re module returns a match object if the string contains the regex pattern, otherwise it returns None.
---

**Contents**

[TOC]

## Introduction

Python's `re` module provides support for regular expressions. Regular expressions are a powerful tool for pattern matching in strings. In this tutorial, we will learn how to use the `re` module to check if a string contains a regex pattern and return True if it matches.

## Importing the re module

The first step is to import the `re` module. The module provides various functions that we can use to work with regular expressions. We import the re module with the following code:

```python
import re
```

## Using re.search() to check if a string contains a regex pattern

The `re.search()` function is used to search for a regex pattern in a string. It returns a match object if it finds a match, and None if it does not. We can use the `re.search()` function to check if a string contains a regex pattern and return True if it does. Here's an example:

```python
import re

string = "The quick brown fox jumps over the lazy dog"
pattern = "brown"

result = re.search(pattern, string)

if result:
    print("Pattern found in the string")
else:
    print("Pattern not found in the string")
```

In this example, we define a string variable and a pattern variable. We then use `re.search()` to search for the pattern in the string. If the pattern is found, `re.search()` returns a match object, which is not None, and the if statement evaluates to True. We print "Pattern found in the string". If the pattern is not found, `re.search()` returns None, and the if statement evaluates to False. We print "Pattern not found in the string".

## Using re.match() to check if a string contains a regex pattern

The `re.match()` function is similar to `re.search()`, but it only searches at the beginning of the string. If the pattern matches the beginning of the string, `re.match()` returns a match object. Otherwise, it returns None. We can use the `re.match()` function to check if a string starts with a regex pattern and return True if it does. Here's an example:

```python
import re

string = "The quick brown fox jumps over the lazy dog"
pattern = "^The"

result = re.match(pattern, string)

if result:
    print("Pattern found at the beginning of the string")
else:
    print("Pattern not found at the beginning of the string")
```

In this example, we define a string variable and a pattern variable. We then use `re.match()` to search for the pattern at the beginning of the string. If the pattern is found at the beginning of the string, `re.match()` returns a match object, which is not None, and the if statement evaluates to True. We print "Pattern found at the beginning of the string". If the pattern is not found at the beginning of the string, `re.match()` returns None, and the if statement evaluates to False. We print "Pattern not found at the beginning of the string".

## Conclusion

In this tutorial, we learned how to use the `re` module to check if a string contains a regex pattern and return True if it matches. We first imported the `re` module, and then used the `re.search()` and `re.match()` functions to search for patterns in strings. We used if statements to check if a pattern was found, and printed the appropriate message.
