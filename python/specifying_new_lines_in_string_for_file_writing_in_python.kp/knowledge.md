---
title: What is the syntax for adding line breaks to a string so that multiple lines can be written to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the escape character `\n` to specify new lines in a string.
---

**Contents**

[TOC]

# Using \n

The \n character can be used to indicate a new line when writing a string to a file in Python. For example:

```
text = "This is the first line\nThis is the second line\nThis is the third line"
```

# Using Triple Quotes

Using triple quotes (either single or double) can also be used to write multiple lines to a file in Python. For example:

```
text = """This is the first line
This is the second line
This is the third line"""
```

# Using join()

The join() method can be used to combine multiple strings into a single string, with each string separated by a new line. For example:

```
lines = ["This is the first line", "This is the second line", "This is the third line"]
text = "\n".join(lines)
```

# Using format()

The format() method can also be used to write multiple lines to a file. For example:

```
text = "This is the first line\n{}\nThis is the third line".format("This is the second line")
```
