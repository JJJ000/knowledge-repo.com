---
title: Invoke a Python function from within jinja2
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can call a Python function from jinja2 using a custom filter.
---

**Contents**

[TOC]

Introduction
------------

Jinja2 is a powerful templating engine for Python. It allows developers to define templates and then use these templates to generate formatted text output. However, there may be times when developers need to call a Python function in the context of a Jinja2 template. This can be accomplished using a combination of Jinja2's built-in features and Python's dynamic capabilities.

How to call a Python function from Jinja2
-----------------------------------------

To call a Python function from Jinja2, we need to follow these steps:

1. Create a Python function that returns the desired output.
2. Import the function into the Jinja2 environment.
3. Call the function from the Jinja2 template.

Creating a Python Function
--------------------------

First, let's create a simple Python function that takes a string as input and returns it in uppercase. We'll call this function `to_upper()`:

```python
def to_upper(string):
    return string.upper()
```

Importing the Function
----------------------

Now that we have our function, we need to import it into the Jinja2 environment. To do this, we create a Python module that contains our function and then import this module into the Jinja2 environment. Here's an example Python module:

```python
# my_functions.py
def to_upper(string):
    return string.upper()
```

To import this module into our Jinja2 environment, we need to create a `CustomEnvironment` object that specifies the module's location:

```python
from jinja2 import Environment, FileSystemLoader
from my_functions import to_upper

env = Environment(loader=FileSystemLoader('templates'))
env.globals.update(to_upper=to_upper)
```

This code creates a `CustomEnvironment` object that loads templates from the `templates` directory. We then import `to_upper()` from the `my_functions` module and add it to the Jinja2 environment's global namespace. This makes `to_upper()` available to all templates that use this environment.

Calling the Function from the Jinja2 Template
--------------------------------------------

Now that we have our function defined and imported into the Jinja2 environment, we can call it from a template. In the template, we use the `to_upper()` function like any other Jinja2 filter:

```
{{ my_string|to_upper }}
```

Here, `my_string` is a variable that contains the string we want to convert to uppercase. The `to_upper` filter applies the `to_upper()` function to `my_string`.

Conclusion
----------

In this post, we explained how to call a Python function from a Jinja2 template. We saw that this can be achieved by creating a Python module that contains our function, importing the module into a Jinja2 environment, and then calling the function from a template. By using this technique, developers can take advantage of the full power of Python within their Jinja2 templates.
