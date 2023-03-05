---
title: Determine the quantity of times a subsequence appears within a larger sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the count() method on the string to count the number of occurrences of a substring.
---

**Contents**

[TOC]

# Splitting the string

The easiest way to count the number of occurrences of a substring in a string in Python is to split the string using the substring as the delimiter. This will give you a list of parts that make up the string, including the parts that contain the substring. You can then count the number of parts in the list to get the number of occurrences of the substring.

Here's an example:

```python
string = "Hello, how are you doing today? I hope you are doing well."
substring = "you"

parts = string.split(substring)
count = len(parts)-1

print("The substring '{}' occurs {} times in the string".format(substring, count))
```

Output:

```
The substring 'you' occurs 2 times in the string
```

# Using regular expressions

Another way to count the number of occurrences of a substring in a string in Python is to use regular expressions. The `re` module provides functions for working with regular expressions.

Here's an example:

```python
import re

string = "Hello, how are you doing today? I hope you are doing well."
substring = "you"

pattern = re.compile(substring)
matches = pattern.findall(string)
count = len(matches)

print("The substring '{}' occurs {} times in the string".format(substring, count))
```

Output:

```
The substring 'you' occurs 2 times in the string
```

# Using count() method

Python also provides the `count()` method that returns the number of occurrences of a substring in a string.

Here's an example:

```python
string = "Hello, how are you doing today? I hope you are doing well."
substring = "you"

count = string.count(substring)

print("The substring '{}' occurs {} times in the string".format(substring, count))
```

Output:

```
The substring 'you' occurs 2 times in the string
```

# Using list comprehension

One more way to count the number of occurrences of a substring in a string is to use list comprehension. 

Here's an example:

```python
string = "Hello, how are you doing today? I hope you are doing well."
substring = "you"

count = len([i for i in range(len(string)-len(substring)+1) if string[i:i+len(substring)] == substring])

print("The substring '{}' occurs {} times in the string".format(substring, count))
```

Output:

```
The substring 'you' occurs 2 times in the string
```

Note: The list comprehension creates a list of indices where the substring matches the string, and then calculates the length of this list.
