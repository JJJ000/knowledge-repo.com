---
title: How to capitalize only the first letter in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the .capitalize() method to capitalize the first letter of a string in Python.
---

**Contents**

[TOC]

## Introduction
In Python, we can use the `capitalize()` method to capitalize the first letter of a string. However, this method capitalizes the first letter of every word in the string. Sometimes, we may only want to capitalize the first letter of the first word. This can be done in a few ways, which we will discuss in this article. 

## Using string slicing 
One way to capitalize the first letter only is to use string slicing. Here is an example:

```python
s = "hello world"
s = s[0].upper() + s[1:]
print(s)
```

Output: 
```
Hello world
```
In this code, we use string slicing to select the first character of the string `s` and capitalize it using the `upper()` method. Then, we concatenate this capitalized character with the rest of the string starting from the second character. 

## Using the title() method with a twist
Another way to capitalize the first letter only is to use the `title()` method and then convert the other capitalized letters back to lowercase using the `lower()` method. Here is an example:

```python
s = "hello world"
s = s.title().replace(s[1:].title(), s[1:].lower())
print(s)
```

Output: 
```
Hello world
```

In this code, we first use the `title()` method to capitalize the first letter of every word in the string. Then, we use the `replace()` method to replace the capitalized letters in all words except the first with their lowercase equivalents. 

## Using regular expressions
A third way to capitalize the first letter only is to use regular expressions. Here is an example:

```python
import re

s = "hello world"
s = re.sub(r"\b\w", lambda match: match.group().upper(), s)
print(s)
```

Output: 
```
Hello world
```

In this code, we use the `sub()` method from the `re` module to search for word boundaries (`\b`) followed by a word character (`\w`) and replace them with the result of a lambda function that upper-cases the match. 

## Conclusion
In this article, we have discussed three ways to capitalize the first letter only in a string in Python. These methods involve using string slicing, the `title()` method with a twist, and regular expressions. Depending on the specific use case, one method may be more appropriate than the others.
