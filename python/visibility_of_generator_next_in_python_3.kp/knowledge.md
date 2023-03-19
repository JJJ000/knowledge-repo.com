---
title: Can generator.next() be accessed in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Yes, generator.next() is visible in Python 3, but it has been renamed to generator.\_\_next\_\_().
---

**Contents**

[TOC]

No

Python 3 introduced a change to the behavior of generators when using the `generator.__next__()` method. The new syntax is `generator.__next__()`. The old syntax `generator.next()` no longer works.

Compatibility issues

While the `generator.__next__()` method is compatible with Python 2 and 3, the old syntax `generator.next()` is not. If you need to maintain compatibility with earlier Python versions, it is recommended to use the new syntax.

Benefits

Using the new syntax consistently ensures that you won't accidentally use the old syntax and introduces simplicity in development. It ensures that the right syntax is being used across various Python versions.

Conclusion

The `generator.__next__()` method is the preferred syntax to use with generators in Python 3. While the old syntax `generator.next()` may work in earlier Python versions, it is not compatible with Python 3.
