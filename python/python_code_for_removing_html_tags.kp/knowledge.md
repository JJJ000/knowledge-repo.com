---
title: Rewrite a programming code in Python language that eliminates html tags contained in a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the Python library BeautifulSoup to parse the string and remove any HTML tags.
---

**Contents**

[TOC]

## Introduction
In this article, we will discuss how to remove HTML tags from a string using Python. 

## Using Regular Expressions
One of the efficient ways to remove HTML tags from a string is by using regular expressions. Below is the Python code for the same:

```python
import re

def remove_html_tags(text):
    clean = re.compile('<.*?>')
    return re.sub(clean, '', text)

sample_text = '<p>This is a sample text with HTML tags</p>'
print(remove_html_tags(sample_text))
```

The `remove_html_tags()` function compiles a regular expression pattern that matches any sequence of characters (.*), which is between an opening angle bracket (<) and a closing angle bracket (>). This pattern is then used to replace the matched sequences with an empty string.

## Using BeautifulSoup
Another way to remove HTML tags from a string is by using the BeautifulSoup library. Below is the Python code for the same:

```python
from bs4 import BeautifulSoup

def remove_html_tags(text):
    soup = BeautifulSoup(text, 'html.parser')
    return soup.get_text()

sample_text = '<p>This is a sample text with HTML tags</p>'
print(remove_html_tags(sample_text))
```

The `remove_html_tags()` function uses the `BeautifulSoup` constructor to create a BeautifulSoup object from the input text. The `get_text()` method is then used to get the plain text content of the HTML string, without any HTML tags.

## Using lxml
Another Python library that can be used to remove HTML tags from a string is lxml. Below is the Python code for the same:

```python
from lxml import etree

def remove_html_tags(text):
    parser = etree.HTMLParser()
    tree = etree.fromstring(text, parser)
    return etree.tostring(tree, encoding='unicode', method='text')

sample_text = '<p> This is a sample text with HTML tags</p>'
print(remove_html_tags(sample_text))
```

The `remove_html_tags()` function uses the `HTMLParser` class from lxml to parse the input text as HTML. An ElementTree is then created from the parsed HTML using the `etree.fromstring()` method. Finally, the `etree.tostring()` method is used to generate a string representation of the ElementTree, which contains only the text content of the input HTML, without any HTML tags.
