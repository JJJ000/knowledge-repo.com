---
title: Can a long line of code be split into multiple lines in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, it is possible to break a long line to multiple lines in Python by using the line continuation character (\) at the end of each line.
---

**Contents**

[TOC]

**Yes, it is possible to break a long line to multiple lines in Python.**

**Method 1: Use backslash (\)**

The backslash character (\) can be used to break a long line of code into multiple lines. This allows the programmer to spread code across multiple lines for easier readability. For example:

```python
total_cost = (price_of_item_1 + price_of_item_2 +
              price_of_item_3 + price_of_item_4)
```

**Method 2: Use parentheses ()**

Parentheses can also be used to break a long line of code into multiple lines. This is especially helpful when assigning values to variables. For example:

```python
total_cost = (price_of_item_1 + 
              price_of_item_2 + 
              price_of_item_3 + 
              price_of_item_4)
```

**Method 3: Use brackets []**

Brackets can be used to break a long line of code into multiple lines. This is especially helpful when assigning values to a list. For example:

```python
shopping_list = [item_1, 
                 item_2, 
                 item_3, 
                 item_4]
```

**Method 4: Use triple quotes (""")**

Triple quotes can be used to break a long line of code into multiple lines. This is especially helpful when writing comments or strings. For example:

```python
message = """
Hello there!
Welcome to my program.
I hope you have a great time.
"""
```
