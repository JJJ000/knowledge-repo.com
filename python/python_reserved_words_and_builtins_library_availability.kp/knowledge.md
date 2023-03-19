---
title: Can a library provide the catalog of Python reserved words and built-ins?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, the list of Python reserved words and builtins is available in the `keyword` and `builtins` library respectively.
---

**Contents**

[TOC]

No, there is no library specifically for Python reserved words and builtins. However, there are ways to access this information through Python itself.

## Python's `keyword` module

Python provides a built-in `keyword` module which can be used to retrieve a list of all reserved words in Python. The following code demonstrates how to use this module:

```python
import keyword

# Get all reserved words
reserved_words = keyword.kwlist

# Check if a word is reserved or not
is_reserved = keyword.iskeyword(word)
```

## Python's `builtins` module

Python also provides a module called `builtins` which contains a list of all the built-in functions, types, and exceptions in Python. The following code demonstrates how to access this information:

```python
import builtins

# Get all built-in functions, types, and exceptions
built_in_names = dir(builtins)
```

## Python documentation

Finally, information about reserved words and built-ins can also be found in the official Python documentation. The [built-in functions](https://docs.python.org/3/library/functions.html) and [built-in types](https://docs.python.org/3/library/stdtypes.html) pages provide an overview of all built-in functions and types respectively. Additionally, the [keywords](https://docs.python.org/3/reference/lexical_analysis.html#keywords) page in the official documentation lists all reserved words in Python.
