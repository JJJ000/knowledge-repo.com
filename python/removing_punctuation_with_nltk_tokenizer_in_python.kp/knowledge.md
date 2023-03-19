---
title: What is the approach to eliminate punctuation with nltk tokenizer?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Set the `strip\_punctuation` parameter to True when initializing the tokenizer object.
---

**Contents**

[TOC]

### Introduction
NLTK is a widely used natural language processing library in Python. One of its functionalities includes tokenizing raw text into individual tokens. However, by default, NLTK tokenizer considers punctuations as separate tokens as well. That might not be desirable for some use cases, so there are ways to get rid of punctuations while tokenizing with NLTK. We will discuss some of those methods in this article.

### Method 1: Using NLTK's Tokenizing Regular Expression
NLTK provides a built-in regular expression for tokenizing text. This regular expression considers punctuations as separate tokens. We can modify this regular expression to exclude punctuation from tokenizing. Here's how:

```python
from nltk.tokenize import RegexpTokenizer

tokenizer = RegexpTokenizer(r'\w+')
tokens = tokenizer.tokenize(raw_text)
```

The `r'\w+'` regular expression matches alphanumeric characters (letters and numbers) and underscores (`_`). So this expression will split the text into tokens by excluding all other characters besides letters, numbers, and underscores.

### Method 2: Using string.punctutation and string.whitespace
Python provides two built-in strings- `string.punctuation` and `string.whitespace`- that include all punctuations and whitespaces, respectively. We can use these strings to create our own tokenizer. Here's how:

```python
import string

def custom_tokenizer(raw_text):
    for punctuation in string.punctuation:
        raw_text = raw_text.replace(punctuation, "")
    tokens = raw_text.split()
    return tokens
```

First, we use a for loop to iterate over every punctuation in `string.punctuation` and replace it with an empty string using the `replace()` method. Then, we split the text into tokens by whitespaces using the `split()` method, and return the tokens.

### Method 3: Using Regular Expressions with string.punctuation
If you don't want to create a custom tokenizer or modify NLTK's built-in tokenizer, you can use regular expressions to filter out punctuations. Here's an example:

```python
import re
import string

def regex_tokenizer(raw_text):
    # Exclude punctuations using regular expression
    raw_text = re.sub('['+string.punctuation+']', '', raw_text)
    tokens = raw_text.split()
    return tokens
```

Here, we use the `re.sub()` method with a regular expression to remove all characters that are in `string.punctuation`. The regular expression is enclosed by square brackets `[]` to create a character class that matches any character inside it.

### Conclusion
In this article, we discussed three ways to get rid of punctuations while tokenizing texts in NLTK. These methods include modifying NLTK's built-in regular expression, creating a custom tokenizer using `string.punctuation` and `string.whitespace`, and using a regular expression with `string.punctuation`. Choose the method that fits your use case and enjoy tokenizing your text!
