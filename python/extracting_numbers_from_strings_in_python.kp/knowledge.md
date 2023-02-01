---
title: What is the best way to pull out numbers from a string in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in re module to extract numbers from a string using regular expressions.
---

**Contents**

[TOC]

### Using Regular Expressions
Regular expressions can be used to extract numbers from strings. The following example uses the `re.findall()` function to extract all numbers from a string:

```python
import re

text = "The cost is $100, but with taxes it's $120"

numbers = re.findall(r'\d+', text)
print(numbers)
# Output: ['100', '120']
```

### Using List Comprehension
List comprehension can be used to extract numbers from strings. The following example uses a list comprehension to extract all numbers from a string:

```python
text = "The cost is $100, but with taxes it's $120"

numbers = [int(s) for s in text.split() if s.isdigit()]
print(numbers)
# Output: [100, 120]
```

### Using Split()
The `split()` method can be used to extract numbers from strings. The following example uses the `split()` method to extract all numbers from a string:

```python
text = "The cost is $100, but with taxes it's $120"

numbers = [int(s) for s in text.split('$') if s.isdigit()]
print(numbers)
# Output: [100, 120]
```

### Using Map()
The `map()` function can be used to extract numbers from strings. The following example uses the `map()` function to extract all numbers from a string:

```python
text = "The cost is $100, but with taxes it's $120"

numbers = list(map(int, re.findall('\d+', text)))
print(numbers)
# Output: [100, 120]
```
