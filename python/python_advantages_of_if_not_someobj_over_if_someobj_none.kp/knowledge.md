---
title: What makes "if not someobj" superior to "if someobj == none" in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The former checks for falsy values while the latter checks for only None.
---

**Contents**

[TOC]

Clarity and Readability

The first reason why `if not someobj:` is better than `if someobj == None:` in Python is because it makes the code more clear and readable. The use of the `not` keyword in the first example makes it immediately clear that we are checking if the object is "falsey" (i.e. equivalent to `False`, `None`, `0`, `""`, etc.), while the second example requires more mental processing to understand that we are specifically checking for `None`.

One-Liner Solution

Another benefit of using `if not someobj:` is that it can be used as a one-liner solution for checking if an object is `None`. For example, the following code:

```
if someobj == None:
    do_something()
```

can be simplified to:

```
if not someobj:
    do_something()
```

This saves a line of code and makes the code more concise.

Compatibility with Falsey Values

Lastly, using `if not someobj:` is more compatible with other "falsey" values besides `None`. This means that if `someobj` is any other value that is equivalent to `False`, the first example will still work as intended. For example, if `someobj` is an empty list, the first example will still evaluate to `True`, while the second example will not.

Overall, using `if not someobj:` is a more clear, concise, and compatible way of checking if an object is "falsey" than using `if someobj == None:`.
