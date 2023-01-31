---
title: What is the best way to capitalize the first letter of each word in a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the str.title() method to capitalize the first letter of each word in a string in Python.
---

**Contents**

[TOC]

### Using capitalize()

The `capitalize()` method can be used to capitalize the first letter of each word in a string.

```python
sentence = 'hello world'

capitalized_sentence = sentence.capitalize()
print(capitalized_sentence)

# Output: Hello world
```

### Using title()

The `title()` method can be used to capitalize the first letter of each word in a string.

```python
sentence = 'hello world'

capitalized_sentence = sentence.title()
print(capitalized_sentence)

# Output: Hello World
```

### Using split() and join()

The `split()` and `join()` methods can be used to capitalize the first letter of each word in a string.

```python
sentence = 'hello world'

words = sentence.split()
capitalized_words = [word.capitalize() for word in words]
capitalized_sentence = ' '.join(capitalized_words)
print(capitalized_sentence)

# Output: Hello World
```

### Using regex

The `re` module can be used to capitalize the first letter of each word in a string.

```python
import re

sentence = 'hello world'

capitalized_sentence = re.sub(r"\b[a-z]", lambda m: m.group(0).upper(), sentence)
print(capitalized_sentence)

# Output: Hello World
```
