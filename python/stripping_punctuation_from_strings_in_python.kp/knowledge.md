---
title: How to remove punctuation from a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The best way to strip punctuation from a string in Python is to use the `str.translate()` method.
---

**Contents**

[TOC]

**Using Regular Expressions:**

1. Import the `re` module: `import re`
2. Create a regular expression for punctuation: `punctuation = re.compile('[.,!?\\-]')`
3. Use the `sub()` function to replace all punctuation with an empty string: `string = punctuation.sub('', string)`

**Using String Replace:**

1. Import the `string` module: `import string`
2. Create a string of all punctuation: `punctuation = string.punctuation`
3. Use the `replace()` function to replace all punctuation with an empty string: `string = string.replace(punctuation, '')`

**Using List Comprehension:**

1. Create a list of all punctuation: `punctuation = ['.', ',', '!', '?', '-']`
2. Iterate through the characters in the string and remove all punctuation: `string = ''.join([char for char in string if char not in punctuation])`
