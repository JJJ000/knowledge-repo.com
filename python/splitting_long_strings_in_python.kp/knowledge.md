---
title: What is the best way to divide a lengthy string into multiple lines?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the backslash character (\) at the end of each line to indicate that the string continues on the next line.
---

**Contents**

[TOC]

**Using Parentheses** 

One way to split a long string over multiple lines in Python is to use parentheses. By enclosing the string in parentheses, Python will ignore the line break and treat the string as a single entity.

Example: 
```
long_string = ("This is a long string that we want to split over multiple lines. "
               "It can be done quite easily with parentheses.")
```

**Using Backslashes** 

Another way to split a long string over multiple lines in Python is to use backslashes. By adding a backslash at the end of each line, Python will ignore the line break and treat the string as a single entity.

Example: 
```
long_string = "This is a long string that we want to split over multiple lines. \
It can be done quite easily with backslashes."
```

**Using Triple Quotes** 

A third way to split a long string over multiple lines in Python is to use triple quotes. By enclosing the string in triple quotes, Python will ignore the line break and treat the string as a single entity.

Example: 
```
long_string = """This is a long string that we want to split over multiple lines. 
It can be done quite easily with triple quotes."""
```

**Using the Line Continuation Character** 

Finally, a fourth way to split a long string over multiple lines in Python is to use the line continuation character. By adding a backslash at the end of each line and using the plus sign at the beginning of the next line, Python will ignore the line break and treat the string as a single entity.

Example: 
```
long_string = "This is a long string that we want to split over multiple lines. \
+It can be done quite easily with the line continuation character."
```
