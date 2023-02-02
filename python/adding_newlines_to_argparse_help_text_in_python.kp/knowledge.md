---
title: What is the best way to add line breaks to argparse help text?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `\\n` escape sequence to add newlines in argparse help text.
---

**Contents**

[TOC]

## Using \n

The simplest way to insert a newline in an argparse help text is to use the `\n` escape character. This will insert a newline character at the position of the `\n` in the string. For example:

```python
parser.add_argument('--example', help="This is an example\nof a help text with a newline.")
```

## Using Formatter

The `argparse` module also provides a `formatter_class` keyword argument that can be used to specify a custom formatter class. This class must be a subclass of `argparse.HelpFormatter`. This allows you to customize how the help text is formatted.

For example, you can use the `_split_lines` method of the `HelpFormatter` class to manually split the help text into multiple lines. For example:

```python
class MyHelpFormatter(argparse.HelpFormatter):
    def _split_lines(self, text, width):
        return text.split('\n')

parser.add_argument('--example', help="This is an example\nof a help text with a newline.", formatter_class=MyHelpFormatter)
```

## Using Raw Strings

Another way to insert a newline in an argparse help text is to use a raw string. A raw string is a string that starts with `r` and is not interpreted by Python. This allows you to use the `\n` escape character directly in the string without having to escape it. For example:

```python
parser.add_argument('--example', help=r"This is an example\nof a help text with a newline.")
```

## Using Triple Quotes

You can also use triple quotes to create a multi-line string. This is useful if you need to insert multiple newlines in the help text. For example:

```python
parser.add_argument('--example', help="""This is an example
of a help text
with multiple
newlines.""")
```
