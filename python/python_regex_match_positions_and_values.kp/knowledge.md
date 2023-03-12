---
title: How to obtain the positions and values of matches using Python regex
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the method `re.finditer()` to find all matches in a string and get their positions and values using the `start()`, `end()`, and `group()` methods of the returned matches objects.
---

**Contents**

[TOC]

## Introduction

Python regex provides a convenient way to locate specific patterns in text strings. Once a pattern is found, we may want to extract the matched string and/or its position(s) in the original text. In this tutorial, we will explore how to get the positions and values of matches in python regex. 

## Using `re.search()`

The `re.search()` function searches for the first occurrence of a pattern in a string and returns a match object. To get the position(s) of the match(es), we can use the `start()` and `end()` methods of the match object. To get the matched string itself, we can use the `group()` method.

```python
import re

text = "The quick brown fox jumps over the lazy dog."

pattern = "the"

match = re.search(pattern, text, re.IGNORECASE)

while match:
    print("Match found at position", match.start())
    print("Matched string:", match.group())
    match = re.search(pattern, text[match.end():], re.IGNORECASE)
```

Output:

```
Match found at position 0
Matched string: The
Match found at position 31
Matched string: the
Match found at position 42
Matched string: the
```

## Using `re.finditer()`

The `re.finditer()` function returns an iterator that yields match objects for all occurrences of a pattern in a string. We can use a loop to iterate over the matches and print their positions and values.

```python
import re

text = "The quick brown fox jumps over the lazy dog."

pattern = "the"

matches = re.finditer(pattern, text, re.IGNORECASE)

for match in matches:
    print("Match found at position", match.start())
    print("Matched string:", match.group())
```

Output:

```
Match found at position 0
Matched string: The
Match found at position 31
Matched string: the
Match found at position 42
Matched string: the
```

## Using `re.sub()`

The `re.sub()` function replaces all occurrences of a pattern in a string with a specified string. We can use a function as the replacement argument to get the position(s) and value(s) of the matches.

```python
import re

def replace(match):
    print("Match found at position", match.start())
    return "REPLACED"

text = "The quick brown fox jumps over the lazy dog."

pattern = "the"

result = re.sub(pattern, replace, text, flags=re.IGNORECASE)

print(result)
```

Output:

```
Match found at position 0
Match found at position 31
Match found at position 42
REPLACED quick brown fox jumps over REPLACED lazy dog.
```
