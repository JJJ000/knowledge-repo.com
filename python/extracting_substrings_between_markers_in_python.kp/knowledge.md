---
title: What is the process for obtaining the string between two indicators?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the str.partition() method to extract the substring between two markers in Python.
---

**Contents**

[TOC]

## Using Regular Expressions
Regular expressions provide an easy way to extract the substring between two markers. The following example shows how to extract the substring between two markers `[` and `]`:

```python
import re

text = "This is a sample text [with substring] to demonstrate"

pattern = r"\[(.*?)\]"

match = re.search(pattern, text)

if match:
    substring = match.group(1)
    print(substring)
```

Output:
```
with substring
```

## Using String Slicing
String slicing is another way to extract the substring between two markers. The following example shows how to extract the substring between two markers `[` and `]`:

```python
text = "This is a sample text [with substring] to demonstrate"

start_index = text.find("[")
end_index = text.find("]")

substring = text[start_index+1:end_index]

print(substring)
```

Output:
```
with substring
```
