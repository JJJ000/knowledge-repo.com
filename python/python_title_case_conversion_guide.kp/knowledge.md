---
title: What is the method to change a string into title case using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the title() method on the string.
---

**Contents**

[TOC]

## Introduction
In Python, you can convert a string to Title Case, which means the first letter of each word in the string is capitalized while the rest of the letters are in lowercase. There are different ways of achieving this and we will discuss some of them in this guide.

## Using str.title() method
The easiest way to convert a string to title case in Python is by using the built-in method `.title()`. This method capitalizes the first letter of each word in the string and makes the rest of the letters lowercase.

```python
string = "this is a sample string to convert to title case"
title_case = string.title()
print(title_case)
```

Output:
```
This Is A Sample String To Convert To Title Case
```

## Using String Module
Another way to convert a string to title case is by using the `string` module. The `string.capwords()` function capitalizes the first letter of each word in a string and returns a new string with a title case.

```python
import string

string_to_convert = "this is a sample string to convert to title case"
title_case_string = string.capwords(string_to_convert)
print(title_case_string)
```

Output:
```
This Is A Sample String To Convert To Title Case
```

## Using split() and join() method
You could also convert a string to title case by using the `.split()` method to split the string into words and then `.join()` method to join the words back together with the first letter capitalized.

```python
string_to_convert = "this is a sample string to convert to title case"
words = string_to_convert.split()
capitalized_words = [word.capitalize() for word in words]
title_case_string = " ".join(capitalized_words)
print(title_case_string)
```

Output:
```
This Is A Sample String To Convert To Title Case
``` 

## Conclusion
These are three different methods of converting a string to title case in Python with their examples. Title case is often used in writing headlines, titles, and in the display of proper nouns.
