---
title: See if multiple phrases appear in a single string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, Python provides the `in` keyword to check if multiple strings exist in another string.
---

**Contents**

[TOC]

**Solution 1 - Using `in` Operator**

The `in` operator can be used to check if one or more strings exist in another string.

```python
string1 = "Hello"
string2 = "World"
sentence = "Hello World!"

if string1 in sentence and string2 in sentence:
    print("Both strings exist in the sentence")
```

**Solution 2 - Using `re.search`**

The `re.search` function from the `re` module can be used to search for multiple strings in a single string.

```python
import re

string1 = "Hello"
string2 = "World"
sentence = "Hello World!"

if re.search(string1, sentence) and re.search(string2, sentence):
    print("Both strings exist in the sentence")
```

**Solution 3 - Using `all` Function**

The `all` function can be used to check if all the strings exist in the sentence.

```python
string1 = "Hello"
string2 = "World"
sentence = "Hello World!"

strings = [string1, string2]

if all(string in sentence for string in strings):
    print("Both strings exist in the sentence")
```

**Solution 4 - Using `any` Function**

The `any` function can be used to check if any of the strings exist in the sentence.

```python
string1 = "Hello"
string2 = "World"
sentence = "Hello World!"

strings = [string1, string2]

if any(string in sentence for string in strings):
    print("At least one of the strings exist in the sentence")
```
