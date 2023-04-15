---
title: What is the method to directly load a jinja template from the filesystem?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `FileSystemLoader` class from the `jinja2` module to load the template directly from the filesystem.
---

**Contents**

[TOC]

1. Introduction
In Python, we have the capability of loading Jinja templates directly from the filesystem. This is useful when we want to keep the templates separate from our Python code or when we want to reuse templates across multiple projects.

2. Installing Jinja
Before we can load Jinja templates, we need to install the Jinja package. You can install Jinja using pip, which is the package installer for Python.

```
pip install jinja2
```

3. Loading Templates from Filesystem
Once we have Jinja installed, we can load templates from the filesystem using the `FileSystemLoader` class. This class takes a path to the directory containing the templates and returns a `Template` object that we can use to render the template.

```python
from jinja2 import Environment, FileSystemLoader

# Create a Jinja environment with the appropriate loader
env = Environment(loader=FileSystemLoader('/path/to/templates'))

# Load a template by name
template = env.get_template('my_template.html')

# Render the template with some values
output = template.render(name='World')

# Print the output
print(output)
```

In this example, we first create a Jinja environment with the `FileSystemLoader` pointing to the directory containing our templates. We then load a specific template by name using the `get_template` method. Finally, we render the template with some values using the `render` method and print the output.

4. Conclusion
Loading Jinja templates from the filesystem is a powerful way to reuse templates across multiple projects or to keep templates separate from your Python code. You can load templates from the filesystem using the `FileSystemLoader` class and render them with the `render` method of the `Template` object.
