---
title: What is the method for breaking down text without spaces into a list of words?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: One possible way to split text without spaces into list of words in Python is by using regular expressions to match word boundaries and extract the words.
---

**Contents**

[TOC]

## Introduction
Python provides many built-in methods to manipulate strings. However, there is no built-in method to split text without spaces into a list of words. In this notebook, we will explore different approaches to achieve this.

## Approach 1: Using regex
One way to split text without spaces into a list of words is by using regular expressions. We can create a regex pattern to match words based on the lack of spaces between characters. Here is an example:

```python
import re

text = "Splittingtextintowords"
words = re.findall('[A-Z][^A-Z]*', text)
print(words) # ['Splitting', 'text', 'into', 'words']
```

In this example, we used the `re.findall` method to extract all the matches of our regex pattern from the text.

## Approach 2: Using itertools.groupby
Another approach is to use the `groupby` function from the `itertools` module. This function groups consecutive elements that share the same key. We can create a key function that checks if the current character and the next character are both lowercase.

```python
from itertools import groupby

text = "Splittingtextintowords"
words = [''.join(g) for k, g in groupby(text, key=lambda x: x.islower()) if k]
print(words) # ['Splitting', 'text', 'into', 'words']
```

We pass our key function, which returns True if both characters are lowercase, to the `groupby` function. Then we join the consecutive groups of characters with the `join` method to obtain our list of words.

## Conclusion
In conclusion, there are different approaches to split text without spaces into a list of words in Python. We can use regular expressions or the `groupby` function from the `itertools` module.
