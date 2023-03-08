---
title: How come enclosing a string in parentheses does not create a tuple with the string alone?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: In Python, a comma is required to distinguish a tuple from a string with parentheses.
---

**Contents**

[TOC]

Section 1: Understanding Tuples in Python
In Python, tuples are ordered, immutable data structures. This means that once we create a tuple, we cannot change it. Tuples are created by enclosing comma-separated values within parentheses.

For example, we can create a tuple with three elements like this:
```
my_tuple = (1, "hello", True)
```

Section 2: Parentheses and Tuples
Now, let's consider what happens when we put a single string or value in parentheses in Python. 

For instance, if we create a tuple with a string as it's only element like this:
```
my_string_tuple = ("hello")
```

Surprisingly, this does not create a tuple in Python. Instead, Python interprets this as a string literal enclosed within parentheses. Therefore, `my_string_tuple` is simply a string variable equal to "hello".

Section 3: Creating a Tuple with One Element
To create a tuple with a single element, we must include a comma after the element, even if there is only one element. This is because the parentheses are not enough to create a tuple in Python- a comma must be included to indicate that we intend to create a tuple.

Therefore, `my_tuple = ("hello",)` creates a tuple with a single element: "hello". The comma after the string indicates that this is a tuple, rather than just a string in parentheses.

Section 4: Conclusion
In summary, enclosing a string (or any other value) within parentheses does not create a tuple in Python. To create a tuple with only one element, we must include a comma after the element to differentiate it from a plain string or value.
